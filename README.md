# lita-jira

**lita-jira** is a handler for [Lita](https://github.com/jimmycuadra/lita), to interact with a JIRA issue tracker.

## Installation

Add lita-jira to your Lita instance's Gemfile:

``` ruby
gem "lita-jira"
```

## Configuration

Add the following variables to your lita config file:

```
config.handlers.jira.username = 'your_jira_username'
config.handlers.jira.password = 'a_password'
config.handlers.jira.site     = 'https://your.jira.instance.example.com/'
config.handlers.jira.context  = '' # If your instance is in a /subdirectory, put that here
```

## Usage

Short and simple commands:
```
Lita jira <project key> "<summary>"               # Creates a new issue with <summary> in <project key>
Lita jira <issue ID> "<comment>"                  # Adds <comment> to <issue ID>
Lita jira <issue ID>                              # Shows basic details on <issue ID>
```

Long-form:
```
Lita jira issue new <project key> "<summary>"     # Creates a new issue with <summary> in <project key>
Lita jira issue details <issue ID>                #
Lita jira issue assignee
Lita jira issue assignee @username
Lita jira issue
Lita jira comment new <issue ID> "<comment>"      # Adds <comment> to <issue ID>
```

## License

[MIT](http://opensource.org/licenses/MIT)
