<script>
  import { each } from "svelte/internal";
  import experience from "../data/experience.json";
</script>

<div class="" id="experience">
  <div class="py-5 my-4" />
  <small class="fw-bold text-gainsboro-hover">EXPERIENCE</small>
  <hr />
  {#each experience["jobs"] as job}
    <div class="row py-4">
      <div class="col-lg-1 col-2" data-aos="fade-up-right">
        <a
          href={job["org_website"]}
          target="_blank"
          rel="noreferrer"
          class="text-decoration-none"
        >
          <img src={job["org_logo"]} alt="" class="grayscale-hover w-100" />
        </a>
      </div>
      <div class="col-lg-11 col-12" data-aos="fade-up-left">
        <div class="row py-4">
          <div class="col-6 text-start">
            <div class="h6 fw-bold text-gainsboro-hover">{job["org_name"]}</div>
            <div class="h6 fw-bold">{job["position"]}</div>
          </div>
          <div class="col-6 text-end">
            {#if job["start_date"] != job["end_date"]}
              <div class="h6 fw-light fst-italic">
                {job["start_date"]} - {job["end_date"]}
              </div>
            {:else}
              <div class="h6 fw-light fst-italic">{job["end_date"]}</div>
            {/if}
            <div class="h6 fw-light fst-italic">{job["org_location"]}</div>
          </div>
        </div>
        <div class="h6 pb-4 fw-light">
            <ul>
                {#each job["achievements"] as achievement}
                <li class="py-1">
                    {achievement}
                </li>
                {/each}
            </ul>
        </div>
        {#each job['tools'] as tool}
        <small class="btn btn-outline-aquamarine text-uppercase mb-3"
          >
          {tool}
          </small
        >&emsp;
        {/each}
      </div>
    </div>
  {/each}

  <small class="fw-bold text-gainsboro-hover">ORGANIZATIONS</small>
  <hr />
  {#each experience["groups"] as group}
    <div class="row py-4">
      <div class="col-lg-1 col-2" data-aos="fade-up-right">
        <a
          href={group["org_website"]}
          target="_blank"
          rel="noreferrer"
          class="text-decoration-none"
        >
          <img src={group["org_logo"]} alt="" class="grayscale-hover w-100" />
        </a>
      </div>
      <div class="col-lg-11 col-12" data-aos="fade-up-left">
        <div class="row py-4">
          <div class="col-6 text-start">
            <div class="h6 fw-bold text-gainsboro-hover">
              {group["org_name"]}
            </div>
            <div class="h6 fw-bold">{group["position"]}</div>
          </div>
          <div class="col-6 text-end">
            {#if group["start_date"] != group["end_date"]}
              <div class="h6 fw-light fst-italic">
                {group["start_date"]} - {group["end_date"]}
              </div>
            {:else}
              <div class="h6 fw-light fst-italic">{group["end_date"]}</div>
            {/if}
            <div class="h6 fw-light fst-italic">{group["org_location"]}</div>
          </div>
        </div>
        <div class="h6 pb-4 fw-light">
            <ul>
                {#each group["achievements"] as achievement}
                <li class="py-1">
                    {achievement}
                </li>
                {/each}
            </ul>
        </div>
        {#each group['tools'] as tool}
        <small class="btn btn-outline-aquamarine text-uppercase mb-3"
          >
          {tool}
          </small
        >&emsp;
        {/each}
      </div>
    </div>
  {/each}

  <small class="fw-bold text-gainsboro-hover">COMPETITIONS</small>
  <hr />
  {#each experience["competitions"] as competition}
    <div class="row py-4">
      <div class="col-lg-1 col-2" data-aos="fade-up-right">
        <a
          href={competition["org_website"]}
          target="_blank"
          rel="noreferrer"
          class="text-decoration-none"
        >
          <img
            src={competition["org_logo"]}
            alt=""
            class="grayscale-hover w-100"
          />
        </a>
      </div>
      <div class="col-lg-11 col-12" data-aos="fade-up-left">
        <div class="row py-4">
          <div class="col-6 text-start">
            <div class="h6 fw-bold text-gainsboro-hover">
              {competition["org_name"]}
            </div>
            <div class="h6 fw-bold">{competition["position"]}</div>
          </div>
          <div class="col-6 text-end">
            {#if competition["start_date"] != competition["end_date"]}
              <div class="h6 fw-light fst-italic">
                {competition["start_date"]} - {competition["end_date"]}
              </div>
            {:else}
              <div class="h6 fw-light fst-italic">
                {competition["end_date"]}
              </div>
            {/if}
            <div class="h6 fw-light fst-italic">
              {competition["org_location"]}
            </div>
          </div>
        </div>
        <div class="h6 pb-4 fw-light">
            <ul>
                {#each competition["achievements"] as achievement}
                <li class="py-1">
                    {achievement}
                </li>
                {/each}
            </ul>
        </div>
        {#each competition['tools'] as tool}
        <small class="btn btn-outline-aquamarine text-uppercase mb-3"
          >
          {tool}
          </small
        >&emsp;
        {/each}
      </div>
    </div>
  {/each}
</div>
