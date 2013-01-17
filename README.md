# puppet-timezone

Manage timezone settings via Puppet.

In order to change the linux date please also use the local time class.

## Usage

### Set timezone to UTC
```
    class { 'timezone':
        timezone => 'UTC',
    }
    
    class { 'timezone::localtime':
        timezone => 'UTC',
    }
```

### Set timezone to Europe/Berlin
```
    class { 'timezone':
        timezone => 'Europe/Berlin',
    }
    

    class {'timezone::localtime':
		timezone => 'Asia/Jerusalem',
    }	
```

## Other class parameters
* ensure: present or absent, default: present
* autoupgrade: true or false, default: false. Auto-upgrade package, if there is a newer version
* package: string, default: OS specific. Set package name, if platform is not supported.
* config_file: string, default: OS specific. Set config_file, if platform is not supported.
* zoneinfo_dir: string, default: OS specific. Set zoneinfo_dir, if platform is not supported.
