<script>
    import { onMount, onDestroy } from 'svelte'
    import { Editor } from '@tiptap/core'
    import StarterKit from '@tiptap/starter-kit'
	import { defaultExtensions } from './extensions';
  
    let element
    let editor
  
    onMount(() => {
      editor = new Editor({
        autofocus: true,
        element: element,
        extensions: defaultExtensions,
        content: '',
        onTransaction: () => {
          // force re-render so `editor.isActive` works as expected
          editor = editor
        },
      })
    })
  
    onDestroy(() => {
      if (editor) {
        editor.destroy()
      }
    })
  </script>
  
  
  <div bind:this={element} />
  
  <style>
    button.active {
      background: black;
      color: white;
    }
  </style>