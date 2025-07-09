# Use the official Elixir image
FROM elixir:1.15

# Install Hex and Rebar for dependencies
RUN mix local.hex --force && mix local.rebar --force
WORKDIR /app

# Copy Elixir project files
COPY . .

# Install dependencies and compile
RUN mix deps.get && mix compile
EXPOSE 4000

# Start the Phoenix server
CMD ["mix", "phx.server"]
