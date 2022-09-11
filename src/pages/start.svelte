<script>
  import Howitworks from "./start/how-it-works.svelte";
  import Createprofile from "./start/create-profile.svelte";
  import Keepitclassic from "./start/keep-it-classic.svelte";
  import MultimediaReady from "./start/mutimedia-ready.svelte";
  import Builddapps from "./start/build-dapp.svelte";
  import ConnectModal from "../modals/connect.svelte";
  import WalletHelp from "../modals/wallet-help.svelte";

  let connectDlg = false;
  let walletHelp = false;
</script>

<main>
  <section class="hero min-h-[600px] bg-base-200">
    <div class="hero-content flex-col md:flex-row space-x-16">
      <div class="max-w-md flex-1">
        <h1
          class="text-5xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-[#7B55EC] to-[#FF00E5]"
        >
          compose
          <span class="badge badge-secondary">BETA 11</span>
        </h1>
        <p class="mt-8 mb-4 md:mb-16">
          Create and manage your own permanent web3 profile and permaweb pages
          built on Arweave.
        </p>
        <div class="flex space-x-2">
          <button class="btn btn-primary" on:click={() => (connectDlg = true)}
            >Connect Wallet</button
          >
          <button class="btn btn-outline">Learn more</button>
        </div>
      </div>
      <div class="md:inline-block flex-1 place-items-center">
        <img
          class="w-3/4"
          src="assets/permapageslanding-p-800.png"
          alt="permapages"
        />
      </div>
    </div>
  </section>
  <Howitworks />
  <Createprofile />
  <Keepitclassic />
  <MultimediaReady />
  <Builddapps />
</main>
<ConnectModal bind:open={connectDlg} on:help={() => (walletHelp = true)} />
<WalletHelp bind:open={walletHelp} />
