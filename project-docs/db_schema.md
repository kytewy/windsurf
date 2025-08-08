# Database Schema

## Overview
Canonical source of truth for tables, relations, enums, and data models.

## Database Configuration
- **Database Type:** [PostgreSQL/MySQL/SQLite/MongoDB]
- **Version:** [Specify version]
- **Connection Pool Size:** [If applicable]
- **Indexes:** [Performance-critical indexes]

## Core Tables

### Users Table
```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    email VARCHAR(255) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    first_name VARCHAR(100),
    last_name VARCHAR(100),
    avatar_url TEXT,
    email_verified BOOLEAN DEFAULT FALSE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

**Indexes:**
- `idx_users_email` on `email`
- `idx_users_created_at` on `created_at`

### [Add your domain-specific tables here]

## Relationships

### One-to-Many Relationships
- `users` → `[related_table]` (One user can have many [items])

### Many-to-Many Relationships
- `[table1]` ↔ `[table2]` through `[junction_table]`

## Enums

### User Status
```sql
CREATE TYPE user_status AS ENUM ('active', 'inactive', 'suspended', 'deleted');
```

### [Add your domain-specific enums here]

## Data Models (Application Layer)

### User Model
```typescript
interface User {
  id: number;
  email: string;
  firstName?: string;
  lastName?: string;
  avatarUrl?: string;
  emailVerified: boolean;
  createdAt: Date;
  updatedAt: Date;
}
```

### [Add your domain-specific models here]

## Migration Strategy

### Version Control
- Use sequential migration files: `001_initial_schema.sql`, `002_add_user_profiles.sql`
- Always include both `up` and `down` migrations
- Test migrations on staging before production

### Migration Files Location
```
/migrations
  ├── 001_initial_schema.sql
  ├── 002_add_user_profiles.sql
  └── 003_add_indexes.sql
```

## Data Validation Rules

### User Data
- Email must be valid format and unique
- Password must meet security requirements
- Names should be sanitized for XSS prevention

### [Add your domain-specific validation rules]

## Performance Considerations

### Indexing Strategy
- Primary keys: Automatic indexes
- Foreign keys: Add indexes for join performance
- Query patterns: Index columns used in WHERE, ORDER BY

### Query Optimization
- Use EXPLAIN ANALYZE for slow queries
- Consider pagination for large result sets
- Implement proper connection pooling

## Backup & Recovery

### Backup Strategy
- Daily automated backups
- Point-in-time recovery capability
- Test restore procedures monthly

### Data Retention
- User data: [Specify retention policy]
- Logs: [Specify retention policy]
- Analytics: [Specify retention policy]

## Security Considerations

### Data Protection
- Encrypt sensitive fields at rest
- Use parameterized queries to prevent SQL injection
- Implement proper access controls

### Audit Trail
- Track data modifications with timestamps
- Log access patterns for sensitive data
- Implement soft deletes for important records

---
*Update this schema documentation whenever database changes are made.*
