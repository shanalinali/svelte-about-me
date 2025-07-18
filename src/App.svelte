<script>
  let name = "Shanali Islam";
  let graduationYear = 2027;
  let bio =
    "20 years old. Bangladeshi-American. Arizona local. Aspiring web developer — I want to build software centered on culture, community, and communication.";
  let hobbies = ["Coding", "Community", "Creativity", "Collaboration"];

  import ImageCard from "./lib/ImageCard.svelte";

  let cardData = [
    {
      image: "images/Dancing_Solo.JPEG",
      title: "Dancing",
      description: "I've been doing it since I was young. Fully self-taught!",
    },
    {
      image: "images/Hosting_CultureFest.jpg",
      title: "Hosting Events",
      description:
        "I've emceed for 3 ASU events so far, some with crowds over 1,000! I love the festival vibe.",
    },
    {
      image: "images/Reading_With_Chloe_Gong.jpg",
      title: "Reading",
      description:
        "I can read 500+ pages in a day. Reach out if you want to exchange Goodreads accounts!",
    },
    {
      image: "images/ENHYPEN_Concert.jpg",
      title: "Concerts",
      description:
        "Live music keeps me alive; current album on repeat is down below!",
    },
  ];
</script>

<div class="container">
  <h1>Who is <strong>Shanali Islam</strong>?</h1>
  <p>Meet Me! 👋🏽</p>
  <div class="profile-pic">
    <img
      src="images/Profile_Photo.jpg"
      alt="Shanali Islam modeling for the Sun Devil Campus Bookstore during her freshman year at Arizona State University."
    />
  </div>
  <p>{bio}</p>
  <p>
    <i
      >I'm a current <strong>junior</strong> studying Computer Science and
      Informatics at Arizona State University
      <strong>#ClassOf{graduationYear}</strong></i
    >.
  </p>

  <h2>Shanali Summarized:</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby"><strong>{hobby}</strong></div>
    {/each}
  </div>

  <h2>Explore!</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>

<style>
  h1,
  h2 {
    color: #23022e;
    font-family: "Playfair Display", serif;
  }

  p {
    font-family: Georgia, "Times New Roman", Times, serif;
    font-size: 17px;
    color: #23022e;
  }

  img {
    border: 5px solid #ddd;
    border-radius: 6px;
    padding: 4px;
    width: 200px;
    transition: transform 0.3s ease; /* Images should smoothly maintain the 'transform' transition for .3s */
  }

  img:hover {
    transform: scale(1.1); /* Actually executes the image animation*/
  }

  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #d1abad;
    color: #63474d;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    padding: 10px 15px;
    border-radius: 5px;
    transition: transform 0.3s ease; /* Tells browser to smoothly animate a 'transform' transition for 0.3s */
  }

  .hobby:hover {
    transform: scale(1.1); /* Actually changes the 'hobby' appearances */
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2); /* Adds a shadow when hovering over a 'hobby' */
  }

  .card-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin: 20px;
  }
</style>
