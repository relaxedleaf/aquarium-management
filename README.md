# Aquarium Update - Rails Application

## Quick Start

The app is now set up and ready to run! Here's how to start it:

```bash
cd /home/relaxedleaf/github/aquarium_update
eval "$(rbenv init -)"
bundle exec rails server
```

The app will be available at `http://localhost:3000`

## Setup Summary

✅ **Completed:**
- Ruby 2.7.8 installed via rbenv
- Bundler 1.17.2 installed
- All dependencies installed (nokogiri upgraded to 1.15.7 to avoid glibc issues)
- Database created and migrated

## Running the Application

### Start the Server
```bash
bundle exec rails server
# or shorter:
bundle exec rails s
```

### Access the App
Open your browser to: `http://localhost:3000`

### Stop the Server
Press `Ctrl+C` in the terminal where the server is running

## Common Commands

```bash
# Run Rails console
bundle exec rails console

# Run database migrations
bundle exec rails db:migrate

# Check routes
bundle exec rails routes

# Run tests
bundle exec rails test
```

## Notes

- **Nokogiri**: Upgraded from 1.10.1 to 1.15.7 to avoid glibc compatibility issues
- **PostgreSQL**: The `pg` gem is commented out in the Gemfile (production only). Uncomment it if you need PostgreSQL support and install `libpq-dev`
- **Warnings**: You may see some deprecation warnings from older gems - these are harmless

## Troubleshooting

### If you get "command not found: rails"
Make sure rbenv is initialized:
```bash
eval "$(rbenv init -)"
```

### If you need to reinstall dependencies
```bash
bundle install
```

### If database issues occur
```bash
bundle exec rails db:reset  # Drops, creates, and migrates
```
