<script lang="ts">
  import { invoke } from "@tauri-apps/api/tauri"
  import CodeMirror from "svelte-codemirror-editor";
  

  let value = "";
  let name = "";
  let greetMsg = ""

  async function greet(){
    // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
    greetMsg = await invoke("greet", { name })
  }
</script>

<div>
  <CodeMirror bind:value  />
</div>

