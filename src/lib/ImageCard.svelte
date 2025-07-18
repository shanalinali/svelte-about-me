<script>
  export let image; // Image URL prop
  export let title; // Title prop
  export let description; // Description prop
</script>

<div class="card">
  <img src={image} alt={title} />
  <div class="card-content">
    <h2 class="card-title">{title}</h2>
    <p class="card-description">{description}</p>
  </div>
</div>

<style>
  .card {
    background-color: #a790a5;
    border: 1px dashed;
    border-radius: 10px;
    overflow: hidden;
    width: 300px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin: 20px;
    text-align: center;
  }

  .card img {
    width: 100%;
    height: auto;
    transition: transform 0.3s ease; /* Images should smoothly maintain the 'transform' transition for .3s */
  }

  .card img:hover {
    transform: scale(1.1); /* Actually executes the image animation*/
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2); /* Adds a shadow when hovering */
  }

  .card-content {
    padding: 15px;
  }

  .card-title {
    font-size: 1.5em;
    color: #333;
    margin: 0 0 10px 0;
  }

  .card-description {
    font-size: 1em;
    color: #23022e;
    margin: 0;
  }
</style>
