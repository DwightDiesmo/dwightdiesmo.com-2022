<script>
  // import education from 'src/data/education.json';
  import education from "../data/education.json";
  console.log(education["degrees"]);
  education["degrees"][0]["courses"].map((course) => console.log(course));
</script>

<div class="" id="education">
  <div class="py-5 my-4" />
  <small class="fw-bold text-gainsboro-hover">EDUCATION</small>
  <hr />
  {#each education["degrees"] as degree}
    <div class="row">
      <div class="col-lg-1 col-2 pb-4" data-aos="fade-up-right">
        <img src={degree["school_logo"]} alt="" class="grayscale-hover w-100" />
      </div>
      <div class="col-lg-11 col-12" data-aos="fade-up-left">
        <div class="row">
          <div class="col-6 text-start">
            <div class="h6 fw-bold pb-1 text-gainsboro-hover">
              {degree["school_name"]}
            </div>
            <div class="h6 fw-bold">{degree["major"]}</div>
          </div>
          <div class="col-6 text-end">
            <div class="h6 fw-light fst-italic">
              {degree["school_location"]}
            </div>
            {#if degree["start_date"] != degree["end_date"]}
              <div class="h6 fw-light fst-italic">
                {degree["start_date"]} - {degree["end_date"]}
              </div>
            {:else}
              <div class="h6 fw-light fst-italic">{degree["end_date"]}</div>
            {/if}
          </div>
        </div>
        <div class="h6 fw-light py-3">Relevant Coursework:</div>
        <ol>
          <ul>
            {#each degree["courses"] as course}
              <li class="h6 fw-light">&ensp;{course}</li>
            {/each}
          </ul>
        </ol>
      </div>
    </div>
  {/each}
  <!-- {#each education['certifications'] as certificate}
  <div class="row">
    <div class="col-lg-1 col-2 pb-4" data-aos="fade-up-right">
      <img src="/" alt="" class="grayscale-hover w-100" />
    </div>
    <div class="col-lg-11 col-12" data-aos="fade-up-left">
      <div class="row">
        <div class="col-6 text-start">
          <div class="h6 fw-bold pb-1 text-gainsboro-hover">{certificate['school_name']}</div>
          <div class="h6 fw-bold">{certificate['major']}</div>
        </div>
        <div class="col-6 text-end">
          <div class="h6 fw-light fst-italic">{certificate['school_location']}</div>
          {#if certificate['start_date'] != certificate['end_date']}
          <div class="h6 fw-light fst-italic">{certificate['start_date']} - {certificate['end_date']}</div>
          {:else}
          <div class="h6 fw-light fst-italic">{certificate['end_date']}</div>
          {/if}
        </div>
      </div>
      <div class="h6 fw-light py-3">Relevant Coursework:</div>
      <ol>
        <ul>
            {#each certificate['courses'] as course}
            <li class="h6 fw-light">&ensp;{course}</li>
            {/each}
        </ul>
      </ol>
    </div>
  </div>
  {/each} -->
</div>
