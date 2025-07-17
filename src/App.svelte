<script>
  let name = "Constanza";
  let favoriteNumber = 48;
  let bio =
    "I was born in the sunny town of Acapulco in Mexico, July 14, 2005. I lived there up until the age of six, when I moved to San Antonio, TX. I really enjoyed my time there, and after a couple of years I returned to Mexico City where I finished high school. Last year, I moved to Madrid, Spain to study a bachelor's in Economics and Finance at Universidad Francisco de Vitoria. I totally love the culture and the people";
  let hobbies = ["Dancing", "Music", "Reading"];
  import ImageCard from "./ImageCard.svelte";

  let cardData = [
    {
      
      title: "Rubber Duckies",
      description:
        "I love rubber ducks,  whether they're gifts from friends, or from different places I've traveled to, each one carries a fun memory.",
    },
    {
    
      title: "Music",
      description:
        "I love music, every part of it. I love dancing wih my friends, writing songs, and playing the guitar!",
    },
    {
      
      title: "Gymnastics",
      description:
        "I really enjoy tumbling, jumping, and flipping.I've done both competitive gymnastics and cheerleading.",
    },
  ];
</script>

<div class="custom-bg">
  <div class="container">
    <h1>About Me</h1>
    <p>Hello, my name is <strong>{name}</strong>!</p>
    <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
    <p>{bio}</p>

    <h2>My Hobbies</h2>
    <div class="hobbies">
      {#each hobbies as hobby}
        <div class="hobby">{hobby}</div>
      {/each}
    </div>
  </div>

  <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>

<!-- svelte-ignore css_unused_selector -->
<style>
  h1 {
    color: #feffc3;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
    color: #005582;
  }
  h2 {
    color: #feffc3;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
    color: #005582;
  }
  .hobby {
    background-color: #005582;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
    font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
      "Lucida Sans", Arial, sans-serif;
  }

  .custom-bg {
    background-color: #97ebdb;
  }
</style>
