# Provider

Use `kirchdev/discord` `0.10.1` with OpenTofu or Terraform. One bot token covers every guild the bot is in. The bot has to already be a member, and its role has to sit above any role it assigns.

Announcement channels (type 5) and media channels (type 16) are rejected until the guild is a Community server. Use a text channel and say that this is why. Do not try to turn Community on from Terraform. The provider leaves guild feature flags read-only, and Discord has no API for a vanity URL.

The provider's docs are the resource list. Look them up when a field is unclear. The gaps that matter in practice: no directory channels, no audit-log data source, no installed-integration resource.
