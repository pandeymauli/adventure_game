# detective

create text-based games in the style of "Her Story"

### installation
`pip install -r requirements.txt`

### usage
1. be the detective. `python detective.py` (`python detective.py -h` for more info)
2. be the author. `python author.py` (`python author.py -h` for more info)
    * `--mode` options
        * `searches_to_entries`
        * `entries_to_words`
        * `entries_graph`
        * `searches_graph`

### data
stories are defined by yaml files. see example `stories/story_2.yaml`

* intro_text: string. if set, text to display at start of session (optional)
* intro_stats: bool. if set, display some stats about the story at start of session (optional)
* match_count_limit: int. if set, maximum number of entries that can be returned by a search (optional)
* initial_search: string. if set, start the session with an already executed serach for this term (optional)
* entries: sequence of mappings w/ keys. this is the meat of the data
    * id: string. if not set, id will be set to entry's position index in list of entries (optional)
    * date: date|datetime. date for the entry. matches will be returned in order of date ascending
    * text: string. the content of the entry to be displayed

### TODO
detective mode
- [x] basic loop from story file
- [x] search history
- [x] read history of entries. flag unread entries
- [x] display progress % of all entries read
- [ ] persistence

author mode
- [x] common terms
- [x] basic traversals through search terms. beats and threads

extra
- [ ] integrated text adventure. (passwords, text adventure...)
- [ ] interactive elements based on entries uncovered
