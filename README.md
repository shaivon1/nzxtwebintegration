# nzxtwebintegration
const kraken = window.location.search.includes("kraken=1");
if (kraken) {
  // On Kraken Browser
  window.addEventListener("storage", (event) => {
    if (event.key === "greeting") {
      console.log(event.newValue);
    }
  });
} else {
  // On Configration Browser
  window.localStorage.setItem("greeting", "hello from kraken");
}
// Kraken and Configuration Browsers
