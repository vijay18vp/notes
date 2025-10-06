import React from 'react';
import { Send, Paperclip, Smile, Plus } from 'lucide-react';
import ReactMarkdown from 'react-markdown';
import remarkGfm from 'remark-gfm';
import rehypeKatex from 'rehype-katex';
import { Prism as SyntaxHighlighter } from 'react-syntax-highlighter';
import { oneDark } from 'react-syntax-highlighter/dist/esm/styles/prism';
import 'katex/dist/katex.min.css';

🔍 Explanation:
import React from 'react';
➤ React is the core library used to build UI components.
It lets you create components (like buttons, chats, forms) that automatically update when data changes.
{ Send, Paperclip, Smile, Plus } from 'lucide-react'
➤ These are icons (SVGs) used inside buttons — for example ✉️ Send icon, 📎 Attach file icon, 🙂 Emoji icon, ➕ New Chat icon.
You can use them like <Send /> in your JSX.
ReactMarkdown, remarkGfm, rehypeKatex
➤ These are libraries to render Markdown and math in messages.
For example, if a message contains **bold** or equations like E=mc^2, these will display properly formatted.
SyntaxHighlighter + oneDark
➤ Used to highlight code blocks in messages (like when AI sends code).
oneDark is the color theme (same as VS Code dark mode).
'katex/dist/katex.min.css'
➤ Imports CSS styling for math equations so they display beautifully.


2 . 
export default function Chat({ messages = [], isLoading = false, onSendMessage, onNewChat, className = '' }) {
🔍 Explanation:
export default function Chat()
➤ Creates a React functional component named Chat.
This function returns JSX (HTML-like structure) to display the UI.
The parameters inside {} are props (data passed from parent component):
messages → array of chat messages
isLoading → whether AI is typing
onSendMessage → function to send a new message
onNewChat → function to start a new chat
className → extra styling if needed
