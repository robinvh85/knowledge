# ActiveRecord

## Create encrypted field
- Generate keys for encryption
```bash
bin/rails db:encryption:init
```

- File `config/application.rb`:
  - Setup parameter for ActiveRecord

```ruby
config.active_record.encryption.primary_key = Settings.active_record.primary_key
config.active_record.encryption.deterministic_key = Settings.active_record.deterministic_key
config.active_record.encryption.key_derivation_salt = Settings.active_record.key_derivation_salt
```

- In model:
  - Specify encrypted fields

```ruby
encrypts :token, :refresh_token, deterministic: true
```

### Reference
- https://guides.rubyonrails.org/active_record_encryption.html