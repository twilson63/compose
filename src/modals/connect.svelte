<script>
  import { createEventDispatcher } from "svelte";
  import Modal from "../components/modal.svelte";
  export let open;
  const dispatch = createEventDispatcher();
</script>

<Modal bind:open bgColor="bg-white" border="border-4 border-[#929292]">
  <div class="px-[36px] py-[24px] flex flex-col space-y-8">
    <img class="h-[55px] w-[55px]" src="assets/wallet.svg" alt="wallet" />
    <h2 class="text-2xl font-bold text-[#160042]">
      Arweave wallet needed to post
    </h2>
    <p class="text-xl  text-[#160042]">Select your preferred wallet below:</p>
    <button
      class="btn btn-block rounded-full"
      on:click={() => {
        dispatch("connect", { wallet: "arconnect" });
        open = false;
      }}>ArConnect</button
    >
    <button class="btn btn-block rounded-full bg-[#E4E6F1] text-black"
      >Arweave.app</button
    >
    <button
      on:click={() => {
        dispatch("help");
        open = false;
      }}
      class="link no-underline text-center  text-[#160042]"
      >I don't have a wallet</button
    >
  </div>
</Modal>
