# Permissions

Name permissions through the `discord_permission` data source. The `@everyone` role id is the guild id.

Administrator ignores channel overwrites. Say so when the only people who should post are admins: the overwrite stops everyone else, and an admin role still posts.

Read-only channels (announcements, guides) allow view, history, and reactions, and deny sending, threads, attachments, embeds, mentioning everyone, and managing messages.

Chat channels allow view, send, history, reactions, embeds, attachments, and external emoji, and deny mentioning everyone and managing messages.

A forum is a discussion format. A ticket channel that should be a normal channel is a text channel.
