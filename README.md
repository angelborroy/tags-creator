tag-creators
==============

This add-on gives you the ability to restrict Alfresco Repository TAG creation to a specific group of users.

By default, the group the module looks for must have an ID of "GROUP_TAG_CREATORS". The display name can be anything. When you create the group you do not specify "GROUP_"--Alfresco will prepend that for you.

This add-on changes the low-level permissions so that even if someone figures out how to create a TAG without the user interface, the repository tier won't let them do that unless they are in the group.

Compatibility
-------------

This addon has been tested with ACS 7.1, but it should be working from ACS 5.2

Manual Installation
-------------------
There are one "repo-tier" JAR associated with this add-on.

Use `mvn install` to create the JAR in `target` folder.

### Install the JAR

You can install the JAR as you normally would, copying it to `alfresco/webapps/WEB-INF/lib` folder.

### Create and Populate the Group

The TAG_CREATORS group will be created for you automatically. If, for some reason, it does not get created, create a new group with an ID of "GROUP_TAG_CREATORS". You can add individuals and groups to this group. For example, at the very least you will probably want to add ALFRESCO_ADMINISTRATORS to this group.
