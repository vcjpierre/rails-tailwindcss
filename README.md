# Rails + TailwindCSS

## Project Initialization

### Creating a New Rails Application

To create a new Rails application named 'blog' with PostgreSQL as the database and TailwindCSS configured:
```bash
rails new blog -d postgresql -c tailwind
```

## Setting Up TailwindCSS with Rails

TailwindCSS provides utility-first CSS classes to help rapidly build custom designs.

### Add the TailwindCSS Rails gem:

```bash
./bin/bundle add tailwindcss-rails
```

### Install TailwindCSS:

This command sets up the necessary configurations and files for TailwindCSS in your Rails app.
```bash
./bin/rails tailwindcss:install
```

### Build TailwindCSS:

This compiles the CSS for your application.
```bash
rails tailwindcss:build
```

## Running the Application

To start the Rails server:
```bash
./bin/rails server
```

Now, you can navigate to `http://localhost:3000` in your browser to see the running application.

## Database Setup and Model Generation

### Create and Migrate the Database:

Ensure PostgreSQL is running, then create the database and run migrations with:
```bash
rails db:create db:migrate
```

### Generate a Post Scaffold:

This command generates a complete set of model, database migration for that model, controller to manipulate it, views to view and manipulate the data, and a test suite for each of the above:
```bash
rails generate scaffold post title:string content:text
```

After generating new scaffolds, remember to run:
```bash
rails db:migrate
```
to apply the new database schema.