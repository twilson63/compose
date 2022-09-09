<script>
  import { Route, router } from "tinro";
  import Announcer from "./components/announcer.svelte";
  import Transition from "./components/transition.svelte";

  import Start from "./pages/start.svelte";
  import Dashboard from "./pages/dashboard.svelte";
  import About from "./pages/about.svelte";

  import StampProtocol from "./pages/stamps/index.svelte";

  router.mode.hash();
  router.subscribe((_) => window.scrollTo(0, 0));
</script>

<Announcer />
<Transition>
  <Route path="/">
    <Start />
  </Route>
  <Route path="/dashboard">
    <Dashboard />
  </Route>
  <Route path="/about">
    <About />
  </Route>
  <Route path="/stamp-protocol">
    <StampProtocol />
  </Route>
</Transition>
