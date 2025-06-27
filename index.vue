<template>
    <div style="font-family: Arial, sans-serif; max-width: 600px; margin: 50px auto; padding: 20px; border: 1px solid #ccc; border-radius: 10px;">
      <h1 style="text-align: center;">Welcome to My Portfolio</h1>
  
      <div style="margin-top: 30px;">
        <p><strong>Full Name:</strong> Stephen Mutei</p>
        <p><strong>GitHub Username:</strong><p>Solovea-101</p></p>
        <p><strong>Email:</strong> <a :href="`mailto:${email}`" style="color: #007bff;">{{ email }}</a></p>
      </div>
  
      <div style="margin-top: 30px; text-align: center;">
        <h2>Below is my Deployment Link</h2>
        <p>
          <a :href="`https://is-project-4th-year.github.io/build-your-portfolio-github-workflow-essentials-Solovea-101/`" target="_blank" style="color: #007bff; text-decoration: none;">Click here to view my portfolio</a>
        </p>
      </div>
  
      <div style="margin-top: 50px;">
        <h2 style="border-bottom: 2px solid #007bff; padding-top: 5px; padding-bottom: 5px;">3. Learnings from the Git Crash Program</h2>
        <p><strong>What I Thought I'd Learn vs What I Actually Learned</strong></p>
  
       
        <div style="margin-top: 20px;">
          <p><strong>Concept:</strong> Git Branching & Merging</p>
          <p><strong>Expectation 👀:</strong> I thought I’d just review how to create branches and merge them — something I already knew from working on small solo projects.</p>
          <p><strong>Reality 😅:</strong> I quickly discovered there’s <em>much more</em> to it, especially in collaborative workflows. I learned how to name branches meaningfully, when to create them, and how to manage them in an organized way.</p>
          <p><strong>Impact 💡:</strong> This helped me break down my portfolio into manageable features (like a "contact-section" branch), allowing me to work on sections independently and test safely before merging into the main project.</p>
        </div>
  
        
        <div style="margin-top: 20px;">
          <p><strong>Concept:</strong> Pull Requests & Merge Conflicts</p>
          <p><strong>Expectation 👀:</strong> I expected pull requests to be more of a team thing, not very relevant to solo development.</p>
          <p><strong>Reality 😅:</strong> Turns out, pull requests are a great way to <em>review your own changes</em> before merging. And yes — I ran into my first real merge conflict 😅, which taught me how to handle them confidently using the terminal.</p>
          <p><strong>Impact 💡:</strong> This gave me more confidence when syncing changes between feature branches and <code>main</code>, especially after trying experimental changes on my portfolio’s layout.</p>
        </div>
  
        
        <div style="margin-top: 20px;">
          <p><strong>Concept:</strong> GitHub Project Boards, Issues & Milestones</p>
          <p><strong>Expectation 👀:</strong> I thought project boards were overly complex — meant for large teams managing enterprise projects.</p>
          <p><strong>Reality 😅:</strong> It’s literally a visual task board! I could drag my cards between “To Do,” “In Progress,” and “Done.” Issues and milestones helped me set realistic goals and track bugs or enhancements clearly.</p>
          <p><strong>Impact 💡:</strong> Helped me manage each stage of the portfolio — from planning my About section to tracking bugs in layout responsiveness.</p>
        </div>
  
        
        <div style="margin-top: 20px;">
          <p><strong>Concept:</strong> Conventional Commits (fix/docs/style/refactor)</p>
          <p><strong>Expectation 👀:</strong> I didn't think commit messages mattered much — I was used to typing things like “update” or “stuff” 😅.</p>
          <p><strong>Reality 😅:</strong> I learned that using proper prefixes like <code>fix:</code>, <code>style:</code>, <code>docs:</code>, or <code>refactor:</code> makes your Git history <em>readable and professional</em>.</p>
          <p><strong>Impact 💡:</strong> My commit logs for the portfolio now look neat and consistent — making it easier to track what I did and when. It’s a small habit, but it makes a huge difference in keeping the project clean.</p>
        </div>
      </div>

      <!-- Project Screenshots Section -->
    <div style="margin-top: 50px;">
      <h2 style="border-bottom: 2px solid #007bff; padding-bottom: 5px;">Project Screenshots</h2>
      <p>Below are some screenshots of my work with short descriptions.</p>

      <div v-for="(screenshot, index) in screenshots" :key="index" style="margin-top: 30px;">
        <img :src="screenshot.src" :alt="`Screenshot ${index + 1}`" style="width: 100%; max-height: 400px; object-fit: contain; border-radius: 8px; border: 1px solid #ddd;" />
        <p style="margin-top: 10px;"><strong>Description:</strong> {{ screenshot.description }}</p>
      </div>
    </div>
    </div>
  </template>
  
  <script setup>
  const github = 'Solovea'
  const email = 'stephen.mutei@strathmore.edu'

  const screenshots = [
  { src: 'images/branching.png', description: 'Branching with meaningful naming' },
  { src: 'images/conflict.png', description: 'No merge conflict present.' },
  { src: 'images/merge.png', description: 'A successful merge of branches' },
  { src: 'images/mergeconflict.png', description: 'Merge conflict arose and was fixed' },
  { src: 'images/milestone.png', description: 'Milestone with its issues' },
  { src: 'images/milestone2.png', description: 'A different milestone with its own issues.' },
  { src: 'images/projectboard.png', description: 'My project board showing various stages of completion of issues' },
  { src: 'images/pullrequest.png', description: 'Creating of a pull reqquest on GitHub' }
]
  </script>
  