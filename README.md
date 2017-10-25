# BUSTLE Activity Machine

The **BUSTLE Activity Machine** is a tool for tracking activities and various resources related to activities. The core of bustle is a shell around a database on which activities may be CRUD'ed and linked to related objects. Besides activities the system has built-in modeling support contextual items such as resources, individuals and locations.

Activities are defined as events that are clearly designated by a start- and stop-time and having at least one individual as participant. Activities may be related to a physical place, reference a number of virtual resources. It may be retroactively defined or planned for. Activities may be manually defined or they may be automatically generated. An automatically generated activity is clearly different than a manually defined one, but may be "converted" to a manually defined \(confirmed\) activity.

This document describes the API used to interact with activities.
