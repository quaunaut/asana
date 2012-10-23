# Asana python api 

python wrapper for the [Asana API](http://asana.com)

Documentation is available at: [AsanaAPI](http://asana.readthedocs.org/en/latest/index.html)
This project is a work in progress. Here's what's currently available:

- add_project_task
- add_story
- add_tag_task
- create_project
- create_task
- get_basic_auth
- get_project
- get_project_tasks
- get_story
- list_workspaces
- create_task
- update_task
- create_project
- update_project
- update_workspace
- add_project_task
- rm_project_task
- add_story
- get_tags
- get_tag_tasks
- get_task
- list_projects
- list_stories
- list_tasks
- list_users
- list_workspaces
- rm_project_task
- update_project
- update_task
- update_workspace
- user_info

Todo:

- All the things!
- unittests
- Better error handling

Sample:

    from asana import asana
    asana_api = asana.AsanaAPI('YourAsanaAPIKey', debug=True)

    # see your workspaces
    myspaces = asana_api.list_workspaces()  #Result: [{u'id': 123456789, u'name': u'asanapy'}]

    # create a new project
    asana_api.create_project('test project', myspaces[0]['id'])

    # create a new task
    asana_api.create_task('yetanotherapitest', myspaces[0]['id'], assignee_status='later', notes='some notes')

    # add a story to task
    asana_api.add_story(mytask, 'omgwtfbbq')

