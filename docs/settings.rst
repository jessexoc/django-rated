========
Settings
========

Required Settings
=================

You must provide a value for these settings.

RATED_REDIS
-----------

Default: {}

Redis config settings.

This will be passed directly to create a redis.ConnectionPool instance.

Default Settings
================

RATED_DEFAULT_REALM
-------------------

Default: 'default'

The default realm to put rated views into.

RATED_DEFAULT_TIMEOUT
---------------------

Default: 60 * 60

Duration (in seconds) over wich requests are counted.  Any request older than
this is not counted toward rate limiting.

RATED_DEFAULT_LIMIT
-------------------

Default: 100

Limit of how many requests an individual client is permitted in the duration.

RATED_RESPONSE_CODE
-------------------

Default: 429

HTTP Status code to return when a request is rate limited.

RATED_RESPONSE_MESSAGE
----------------------

Default: ''

Content to include in response when a request is limited.

RATED_DEFAULT_WHITELIST
-----------------------

Default: []

A list of IPs which are exempt from rate limiting.

Optional settings
=================


RATED_REALMS
------------

Default: {}

A dict of config dicts for each realm.

RATED_REALM_MAP
---------------

Default: {}

A mapping of URL pattern names to Rated realms.

This allows you to add a url/view into a realm without having to decorate the view.

