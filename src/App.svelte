<script>
  import { Router, Route } from "svelte-routing";

  import Layout1 from "./routes/Layout1/Layout_1.svelte";
  import Layout2 from "./routes/Layout2/Layout_2.svelte";
  import Layout3 from "./routes/Layout3/Layout_3.svelte";
  import Layout4 from "./routes/Layout4/Layout_4.svelte";
  import Layout5 from "./routes/Layout5/Layout_5.svelte";
  import Layout6 from "./routes/Layout6/Layout_6.svelte";
  import Layout7 from "./routes/Layout7/Layout_7.svelte";
  import Layout8 from "./routes/Layout8/Layout_8.svelte";
  import Layout9 from "./routes/Layout9/Layout_9.svelte";
  import Layout10 from "./routes/Layout10/Layout_10.svelte";
  import Layout11 from "./routes/Layout11/Layout_11.svelte";
  import Layout12 from "./routes/Layout12/Layout_12.svelte";
  import Login from "./routes/login.svelte";
  import Signup from "./routes/signup.svelte";
  import Password_forget from "./routes/password_forget.svelte";
  import Pay from "./routes/pay.svelte";

  export let url = "/";
</script>

<Router {url}>
  <div>
    <Route path="/"><Pay /></Route>
    <!-- <Route path="/signup"><Signup /></Route> -->
    <!-- <Route path="/password_forget"><Password_forget /></Route> -->
  </div>
</Router>
