# README

This repo serves as a reference for the infrastructure being built for `the group that is still unnamed`. I am exploring self-hosted options for basic productivity apps that can be used by a team.

## Authentication

[Authentik](https://goauthentik.io/) serves as our auth provider. I am using the basic email + password strategy (to borrow a term from passport.js).

All users are first re-directed to the authentik service to enter their credentials before being forwarded to their specific destination.

This is mostly in place because Affine does not allow us to gate the basic local-storage version of the instance so i have to control access myself. (Kind of annoying but a good learning experience).

I have turned off authentik redirection for mobile/electron apps as this flow breaks their regular auth process.

## Reverse Proxy

For this project I decided to try `Caddy` instead of `Nginx` like I usually do. Actually very easy to setup and a delight to work with.

## Services

### Team Chat

[Mattermost](https://mattermost.com/) === Slack

### Notes

[Affine](https://affine.pro/) === Notion

### Cloud Drive

[bewCloud](https://bewcloud.com/) === Google Drive/Nextcloud

## What Else?

### Version Control

Potential move to Gitlab or Gitea for a selfhosted option. Maybe Codeberg.
