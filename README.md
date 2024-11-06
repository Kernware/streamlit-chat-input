## Modifications from Kernware
* Add suggestions/preset history
* allow keydown to clear the current selection
* remove local JS history, as we use it after rerun, so history will be empty
* small UI changes, fixing colors, border width...

# streamlit-chat-input-advanced

Streamlit component that allows you catch arrow up keyboard event

it implements ability to 
* clear textarea when user press Escape

  ![Example message cleanup on Escape|200x100](example_msg_cleanup.gif)
* allow go back and forth by message history 

    ![Chat history example](example_chat_history.gif)

## Installation instructions

```sh
pip install streamlit-chat-input-advanced
```

## Usage instructions

```python
import streamlit as st

from chat_input_advanced import chat_input_avd

value = chat_input_avd()

st.write(value)
```

## Release Process

Build package:
```
npm --prefix ./chat_input_advanced/frontend run build
```

Create new branch with version
```
git checkout -b "v<verison>"
```

Force push build folder
```
git add -f chat_input_advanced/frontend/build/
```

And then create a new release on github.
