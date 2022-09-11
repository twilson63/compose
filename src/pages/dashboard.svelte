<script>
  import Navbar from "../components/navbar.svelte";
  import WalletDashboard from "../components/wallet-dashboard.svelte";
</script>

<Navbar />
<main>
  <section class="mx-16 pt-8  flex justify-between">
    <div>
      <h1
        class="text-2xl text-transparent bg-clip-text bg-gradient-to-r from-[#7B55EC] to-[#FF00E5]"
      >
        You're all set to create on the Permaweb.
      </h1>
      <p class="text-gray-400">Select your next step below.</p>
      <div class="mt-8 alert flex-col w-[400px]">
        <p class="text-sm text-gray-400">
          Top up with Permaweb storage credits by using these cryptocurrency
          options as well:
        </p>
        <div>
          <img src="assets/solana-logo.svg" alt="" />
          <img src="assets/solana-logo.svg" alt="" />
          <img src="assets/solana-logo.svg" alt="" />
        </div>
      </div>
    </div>
    <WalletDashboard />
  </section>
  <section class="mt-16 mx-16 grid grid-cols-3 gap-4">
    <div
      class="flex items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">create blog post</h3>
      <img src="assets/write.svg" alt="write" />
    </div>
    <div
      class="flex flex-col items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">create your profile</h3>
      <img src="assets/profile.svg" alt="profile" />
    </div>
    <div
      class="flex flex-col items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">post image(s)</h3>
      <img src="assets/images.svg" alt="images" />
    </div>
    <div
      class="flex flex-col items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">upload video(s)</h3>
      <img src="assets/video.svg" alt="video" />
    </div>
    <div
      class="flex flex-col items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">create an NFT</h3>
      <img src="assets/nft.svg" alt="nft" />
    </div>
    <div
      class="flex flex-col items-center justify-center h-[300px] w-[400px] border-2 rounded-md bg-gray-100 hover:drop-shadow"
    >
      <h3 class="text-2xl text-gray-500">upload audio</h3>
      <img src="assets/audio.svg" alt="audio" />
    </div>
  </section>
  <section class="mx-16 mt-16 flex justify-center">
    <button class="btn bg-gradient-to-r from-[#7B55EC] to-[#FF00E5]">
      <img src="assets/create.svg" alt="create" />
      created on compose
    </button>
  </section>
</main>
