# Impersonate.

[Auth0](https://auth0.com/) user impersonation utility for when you need to see
exactly what your customers see.

## Installation

From [gobinaries.com](https://gobinaries.com):

```sh
$ curl -sf https://gobinaries.com/drylikov/impersonate | sh
```

From source:

```sh
$ go get github.com/drylikov/impersonate
```

## Setup

You'll need to set the following "global" (account level) env vars:

```sh
export AUTH0_CLIENT_ID=xxxxxxx
export AUTH0_CLIENT_SECRET=xxxxxxx
```

## Usage

To impersonate a user pass the Client ID of your application (not your account),
the "impersonator" user ID (you), and the ID of the user.

```sh
$ impersonate --account apex-inc --client-id xxxxx --impersonator-id 'github|yyy' 'github|zzz'
```

If this gets annoying or you have multiple applications, you may want to alias in your profile:

```sh
alias impersonate_myapp="impersonate --account apex-inc --client-id xxxxx --impersonator-id 'github|yyy'"
```

Then all you need is:

```sh
$ impersonate_myapp 'github|zzz'
```




































































































































