# Safety

Adopt the guild. Never create one and never delete one.

`prevent_destroy` belongs on channels, categories, roles, and webhooks. A rename or a topic edit is an in-place update. Position fights are what `discord_channel_order` is for, when you use it.

Terraform only destroys what it manages. A channel someone made in the client and never imported is still there after apply. Deleting it is a separate, named request.

Webhook tokens end up in state. Keep state local. A remote backend is its own decision. Outputs that would print a webhook URL stay sensitive.

The token is read from the environment. It is not a Terraform variable printed in a plan, not a commit, and not something to repeat back.
