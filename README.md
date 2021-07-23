# Task List integration for Home Assistant
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

> This simple `task list` integration for Home Assistant allows you to keep track of task/todo list 
> items within Home Assistant and is based one the official 
> [Shopping List Integration](https://www.home-assistant.io/integrations/shopping_list/).
> 
> Your task list will be accessible from the sidebar, and you can optionally add the 
> Task List card to your Lovelace dashboard. 
> 
> With the Conversation integration you can add items to your tasks using voice commands like 
> _"Add change batteries on motion sensor in bedroom to my task list"_.

## Installation
Choose either installation alternative:
1. Install custom repository https://github.com/slomic-smarthytte/task_list.git by following  
[custom repository with HACS](https://hacs.xyz/docs/faq/custom_repositories/), or
2. copy manually [task_list](custom_components/task_list)
folder to `custom_components` folder in your Home Assistant config folder
   
## Persistence
A task list item is being persistent in the `.task_list.json` file stored in your Home Assistant 
config folder and is fully in your own control.

## Domain
This integration creates new domain with name `task_list`

## Services
You can add or remove items from your task list by using the following services:

### `task_list.add_item`
Adds an item to the task list.

| Service data attribute | Optional | Description |
| --- | --- | --- |
| `name` | no | Name of the item to add. _Example: "Change batteries on motion sensor in bedroom"_ |

### `task_list.complete_item`
Marks an item as _completed_ in the tasks. It does not remove the item.

| Service data attribute | Optional | Description |
| --- | --- | --- |
| `name` | no | Name of the item to mark as completed. _Example: "Change batteries on motion sensor in bedroom"_ |

### `task_list.incomplete_item`
Marks an item as _incomplete_ in the task list.

| Service data attribute | Optional | Description |
| --- | --- | --- |
| `name` | no | Name of the item to mark as incomplete. _Example: "Change batteries on motion sensor in bedroom"_ |

### `task_list.complete_all`
Marks all items as _completed_ in the task list. It does not remove the items.

### `task_list.incomplete_all`
Marks all items as _incomplete_ in the task list.