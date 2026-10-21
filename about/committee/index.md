---
layout: page
title: Organizing Committee
---

<style>
  .committee-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 30px;
    margin-top: 20px;
  }

  .committee-card {
    background-color: #fff;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .committee-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  }

  .member-photo {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 15px;
    border: 3px solid #f0f0f0;
  }

  .member-name {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
  }

  .member-role {
    font-size: 0.9em;
    color: #666;
    margin-bottom: 10px;
    font-style: italic;
  }

  .member-bio {
    font-size: 0.9em;
    color: #555;
    margin-bottom: 15px;
    line-height: 1.4;
  }

  .member-links {
    margin-top: auto;
    display: flex;
    gap: 15px;
    justify-content: center;
  }

  .member-links a {
    color: #555;
    font-size: 1.2em;
    transition: color 0.2s;
  }

  .member-links a:hover {
    color: #007bff;
  }

  /* Board: teams sit side by side on a 4-column grid; each team spans one column per member */
  .committee-board {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 30px;
    margin-top: 20px;
    align-items: start;
  }

  .committee-team.span-1 { grid-column: span 1; }
  .committee-team.span-2 { grid-column: span 2; }
  .committee-team.span-3 { grid-column: span 3; }
  .committee-team.span-4 { grid-column: span 4; }

  .committee-team h2 {
    margin-top: 0;
    font-size: 1.3em;
  }

  .committee-team .committee-grid {
    margin-top: 0;
  }

  /* On the 4-column board, reserve two lines for headings so long team
     names (e.g. "Operations and Communications Lead") don't push cards down */
  @media (min-width: 993px) {
    .committee-team h2 {
      line-height: 1.3;
      min-height: 2.6em;
      display: flex;
      align-items: flex-end;
    }
  }

  .committee-team.span-1 .committee-grid { grid-template-columns: minmax(0, 1fr); }
  .committee-team.span-2 .committee-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .committee-team.span-3 .committee-grid { grid-template-columns: repeat(3, minmax(0, 1fr)); }
  .committee-team.span-4 .committee-grid { grid-template-columns: repeat(4, minmax(0, 1fr)); }

  /* Tablets: 2 columns; wider teams wrap their members onto extra rows */
  @media (max-width: 992px) {
    .committee-board { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .committee-team.span-3,
    .committee-team.span-4 { grid-column: span 2; }
    .committee-team.span-3 .committee-grid,
    .committee-team.span-4 .committee-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  }

  /* Phones: everything in a single column */
  @media (max-width: 600px) {
    .committee-board { grid-template-columns: minmax(0, 1fr); }
    .committee-team[class*="span-"] { grid-column: auto; }
    .committee-team[class*="span-"] .committee-grid { grid-template-columns: minmax(0, 1fr); }
  }
</style>

# 2026 Organizing Committee

<!-- Teams are ordered so the 4-column board packs without gaps: span-N = number of members -->
<div class="committee-board">
  <section class="committee-team span-1">
    <h2 id="chair">Chair</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/dima.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Dmitry Lupyan</div>
      <div class="member-role">Schrödinger</div>
      <div class="member-bio">
        Dmitry Lupyan is a Research Scientist, Product Manager and computational chemist with 20 years of experience in drug discovery. Driven by a passion for solving challenging scientific problems, he specializes in developing new tools and scientific software to advance pharmaceutical research. His expertise spans advanced molecular modeling, including molecular dynamics (MD), free energy perturbation (FEP), and binding kinetics.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/dmitry-lupyan-9980468/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-1">
    <h2 id="operations-and-communications-lead">Operations and Communications Lead</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/AK.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Aakankschit (AK) Nandkeolyar</div>
      <div class="member-role">OpenEye, Cadence Molecular Sciences</div>
      <div class="member-bio">
        AK is a Scientific Software Developer on the Hit Identification team at OpenEye, Cadence Molecular Sciences. His work focuses on developing Bayesian optimization approaches to efficiently screen ultra-large chemical spaces using 3D ligand similarity methods. He received his Ph.D. from the University of California Irvine under the supervision of Dr. David Mobley, with Dr. Willem Jespers (University of Groningen, The Netherlands) as a secondary advisor.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/aakankschit-nandkeolyar-838b0b126/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-2">
    <h2 id="marketing-team">Marketing Team</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/Salome.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Salomé Llabrés</div>
      <div class="member-role">University of Barcelona</div>
      <div class="member-bio">
        Salomé Llabrés is a lecturer in Physical Chemistry at the University of Barcelona. Her research focuses on computational methods to target membrane proteins and to design new antimicrobial treatments.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/salom%C3%A9-llabr%C3%A9s-prat/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>

    <div class="committee-card">
      <img src="{{ '/about/committee/photos/ana_caldaruse.jpg' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Ana Caldaruse</div>
      <div class="member-role">Vividion Therapeutics</div>
      <div class="member-bio">
        Ana Caldaruse is a scientist at Vividion Therapeutics. She received her Ph.D. in Pharmacological Sciences from the University of California Irvine under the supervision of Dr. David Mobley, where she developed and applied Separated Topologies (SepTop), a method for predicting the binding affinities of potential drug candidates, and combined it with active learning to prioritize the most promising compounds across large and diverse sets of molecules. She is passionate about making computational tools more accessible to the pharmaceutical industry.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/ana-maria-caldaruse-a6253183/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-1">
    <h2 id="local-organization-team">Local Organization Team</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/tj_paul.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Thomas (TJ) Paul</div>
      <div class="member-role">Gilead Sciences</div>
      <div class="member-bio">
        TJ Paul is a Principal Scientist at Gilead Sciences in the San Francisco Bay Area, where he is a computational modeler supporting drug discovery projects in inflammation, oncology, and virology. He previously worked in the Department of Chemistry at the University of Michigan, where he helped develop automated, scalable relative protein–ligand binding free energy calculations using lambda dynamics. He received his PhD in Chemistry from the University of Miami, where his research used molecular dynamics simulations to study metalloenzymes, protein–ligand interactions, and amyloid fibrils.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/thomas-paul-8ba210421/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-3">
    <h2 id="sponsorship-team">Sponsorship Team</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/jordi_png.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Jordi Juárez-Jiménez</div>
      <div class="member-role">University of Barcelona</div>
      <div class="member-bio">
        Jordi Juárez-Jiménez is an Associate Professor of Physical Chemistry at the University of Barcelona. His research focuses on computational approaches for drug design, with an emphasis on free energy methods and the rational development of molecular glues.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/jordi-ju%C3%A1rez-jim%C3%A9nez-45a20961/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
        <a href="https://www.ub.edu/cmd_lab/welcome" title="website"><i class="fas fa-globe"></i></a>
      </div>
    </div>


    <div class="committee-card">
      <img src="{{ '/about/committee/photos/cesar_mendoza_martinez.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Cesar Mendoza Martinez</div>
      <div class="member-role">University of Dundee</div>
      <div class="member-bio">
        Cesar Mendoza Martinez is a Senior Computational Chemist in the Drug Discovery Unit at the University of Dundee, where he applies molecular dynamics, free energy calculations, and cheminformatics to drug discovery for infectious diseases, including work on understanding drug resistance mutations. He previously worked at the University of Edinburgh, using enhanced-sampling and alchemical free energy simulations to study how small molecules induce disorder-to-order transitions in proteins. He obtained his PhD in Chemical Sciences from the National Autonomous University of Mexico (UNAM), where he worked on the design of quinazoline derivatives against trypanosomatid parasites.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/cesar-mendoza-martinez-0411b3b4/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
        <a href="https://www.dundee.ac.uk/people/cesar-mendoza-martinez" title="website"><i class="fas fa-globe"></i></a>
      </div>
    </div>

    <div class="committee-card">
      <img src="{{ '/about/committee/photos/steven_ayoub.jpg' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Steven Ayoub</div>
      <div class="member-role">Graduate Student, University of California Irvine</div>
      <div class="member-bio">
        Steven Ayoub is a graduate student in Pharmaceutical Sciences in the Mobley Lab at the University of California, Irvine. He is developing a pose-triage pipeline that combines co-folding, docking, molecular dynamics, enhanced sampling and free energy calculations to identify the correct ligand binding mode for binding affinity prediction. He earned his Master’s degree in Chemistry from California State University, Northridge, where he developed an automated workflow for absolute binding free energy calculations. He later interned at OpenEye, Cadence Molecular Sciences, where he helped expand and validate tools for identifying potential off-targets of small molecules.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/steven-ayoub-79b30714a/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-2">
    <h2 id="speakers-team">Speakers Team</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/janet_paulsen.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Janet Paulsen</div>
      <div class="member-role">NVIDIA</div>
      <div class="member-bio">
        Janet Paulsen is a Senior Alliance Manager for Drug Discovery at NVIDIA, where she leads strategic partnerships that bring accelerated computing and AI to pharmaceutical research. A computational chemist with over 20 years of experience, she earned her PhD in Pharmaceutical Sciences from the University of Connecticut, focusing on X-ray crystallography and structure-based drug design, and completed postdoctoral research at UMass Chan Medical School studying inhibitor recognition and drug resistance in HIV-1 protease. She then spent several years at Schrödinger as a scientist and marketing manager, where her work included evaluating free energy calculations for prioritizing macrocycle synthesis.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/janetpaulsen/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>

    <div class="committee-card">
      <img src="{{ '/about/committee/photos/martin_voegele.png' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Martin Vögele</div>
      <div class="member-role">Schrödinger</div>
      <div class="member-bio">
        Martin Vögele is a principal scientist in the life science software department at Schrödinger, Inc. in New York City. Previously, he worked as a postdoctoral researcher in computer science at Stanford University on simulations of G protein-coupled receptors and machine learning for structural biology and drug discovery. Before moving to the United States, he obtained a PhD in physics for work on diffusion and self-organization in lipid membranes at the Max Planck Institute of Biophysics in Frankfurt, Germany.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/martin-voegele/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
        <a href="https://bsky.app/profile/martinvoegele.bsky.social" target="_blank" title="Bluesky"><i class="fab fa-bluesky"></i></a>
        <a href="https://martinvoegele.github.io/" title="website"><i class="fas fa-globe"></i></a>
      </div>
    </div>
  </div>
  </section>

  <section class="committee-team span-2">
    <h2 id="blind-challenge-team">Blind Challenge Team</h2>
  <div class="committee-grid">
    <div class="committee-card">
      <img src="{{ '/about/committee/photos/jenke-min.jpeg' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Jenke Scheen</div>
      <div class="member-role">Open Molecular Software Foundation</div>
      <div class="member-bio">
        Jenke is a scientist who broadly applies and develops computational tools and benchmarks for biotechs and pharmaceutical companies. He holds a PhD from the University of Edinburgh in physics-based and data-driven predictive modelling. Previously at ASAP Discovery and CHARM Therapeutics, he currently supports early-stage discovery programs for a variety of institutions.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/jenkescheen/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>

    <div class="committee-card">
      <img src="{{ '/about/committee/photos/Alzbeta.JPG' | relative_url }}" alt="Member Name" class="member-photo">
      <div class="member-name">Dr. Alzbeta Kubincova</div>
      <div class="member-role">University of California Irvine</div>
      <div class="member-bio">
        Alžbeta Kubincová is a postdoc in David Mobley's lab at the University of California, Irvine. Her research interest include free-energy calculations and active learning strategies for drug discovery.
      </div>
      <div class="member-links">
        <a href="https://www.linkedin.com/in/al%C5%BEbeta-kubincov%C3%A1/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
  </section>
</div>
