# OpenStack Redis Module

Marton Kiss <marton.kiss@gmail.com>
Sebastian Marcet <smarcet@gmail.com>

# Quick Start

To install Redis server and configure it with defaults,
include the following in your manifest file:

    class { 'redis':
    }

# Configuration

This module supports redis version 2.2.x, 2.4.x and 2.6.x on Ubuntu
Operation Systems.

## Redis server

    class { 'redis':
      redis_port        => '6379',
      redis_bind        => '127.0.0.1',
      redis_password    => 'mys3cr3tpassw0rd',
      redis_max_memory  => '1gb',
      version           => '2.2.12',
    }

NOTE: you must specify the package version number, because the configuration
templates are different for major redis versions.