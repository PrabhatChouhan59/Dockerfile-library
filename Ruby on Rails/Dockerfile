# Use the official Ruby image
FROM ruby:3.2

# Install dependencies for Rails and Node.js for asset compilation
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
WORKDIR /myapp

# Copy Gemfile and Gemfile.lock for dependency installation
COPY Gemfile* ./
RUN bundle install

# Copy the rest of the application
COPY . .
EXPOSE 3000

# Start the Rails server
CMD ["rails", "server", "-b", "0.0.0.0"]
