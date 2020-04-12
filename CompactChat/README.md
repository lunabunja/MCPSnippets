# Compact Chat
### Compacts down chat.
**Original CompactChat is made by Sk1er**

## Description
#### Compacts duplicate messages.

# How To Use
In GuiNewChat.java change printChatMessage(ITextComponent chatComponent) to:
```java
    public void printChatMessage(ITextComponent chatComponent)
    {
    	if (chatComponent.getUnformattedText().equals(lastMessage)) {
    		Minecraft.getMinecraft().ingameGUI.getChatGUI().deleteChatLine(line);
    		sameMessageAmount++;
    		lastMessage = chatComponent.getUnformattedText();
    		chatComponent.appendText(ChatFormatting.GRAY + " (" + sameMessageAmount + ")");
    	} else {
    		sameMessageAmount = 1;
    		lastMessage = chatComponent.getUnformattedText();
    	}
    	
    	line++;
    	
    	if (line > 256) {
    		line = 0;
    	}
    	
        this.printChatMessageWithOptionalDeletion(chatComponent, line);
    }
```