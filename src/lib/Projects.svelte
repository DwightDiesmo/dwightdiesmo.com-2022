<script>
  import { each } from "svelte/internal";
  import projects from "../data/projects.json";
</script>

<div class="container" id="projects">
  <div class="py-5 my-4" />
  <h2 class="fw-bold text-center text-gainsboro py-5">ENGINEERING PROJECTS</h2>
  <div class="row">
    {#each projects as project}
      <div class="col-lg-4 col-md-6 col-12 py-3" data-aos="fade-up">
        <div class="bg-raisin hover-box-shadow square-card py-5 px-4">
          <a
            href={project["project_repo"]}
            target="_blank"
            rel="noreferrer"
            class="text-gainsboro-hover text-decoration-none"
          >
            <div class="row">
              <div class="col-6 text-start">
                <i class="fa-regular fa-folder fa-3x text-aquamarine" />
              </div>
              <div class="col-6 text-end">
                <i class="fa-brands fa-github fa-1x text-silver-hover" />
              </div>
            </div>
            <div class="row">
              <div class="h4 fw-bold pt-3">{project["project_name"]}</div>
              <div class="h5 truncate fw-normal text-silver py-2">
                {project["project_description"]}
              </div>
            </div>
            <div class="row">
              <div class="h6 text-aquamarine">
                {#each project["project_categories"] as category}
                  {category}&ensp;
                {/each}
              </div>
              <small class="text-silver">
                {#each project["project_tech"] as tech}
                  {tech}&ensp;
                {/each}
              </small>
            </div>
          </a>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>
  .truncate {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
</style>
