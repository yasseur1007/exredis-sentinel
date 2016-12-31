# ExredisSentinel

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed as:

  1. Add configuration on `config/config.exs`

    ```
    config :exredis_sentinel,
      redis_master_name: "redis_master_name",
      sentinnels: [
        { host: "sentinel_host.com", port: 26379 },
        { host: "sentinel_host2.com", port: 26380 }
      ],
      failover_reconnect_timeout: 20,
      namespace: 'your-namespace'
    ```

  2. Add `exredis_sentinel` to your list of dependencies in `mix.exs`:

    ```elixir
    def deps do
      [{:exredis_sentinel, "~> 0.1.0"}]
    end
    ```

  3. Ensure `exredis_sentinel` is started before your application:

    ```elixir
    def application do
      [applications: [:exredis_sentinel]]
    end
    ```

  4. use it like you would use Exredis but use ExredisSentinel

