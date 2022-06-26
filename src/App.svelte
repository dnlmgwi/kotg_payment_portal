<script>
  import { Router, Route } from "svelte-routing";

  import Login from "./routes/login.svelte";
  import Signup from "./routes/signup.svelte";
  import Password_forget from "./routes/password_forget.svelte";
  import Pay from "./routes/pay.svelte";
  import PaymentSuccess from "./routes/payment-success.svelte";

  export let url = "/";
</script>

<Router {url}>
  <div>
    <Route path="/payment-success"><PaymentSuccess /></Route>
    <!-- <Route path="/1"><Layout1 /></Route> -->
    <!-- <Route path="/2"><Layout2 /></Route> -->
    <Route path="/"><Pay /></Route>
    <!-- <Route path="/signup"><Signup /></Route> -->
    <!-- <Route path="/password_forget"><Password_forget /></Route> -->
  </div>
</Router>
