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
  </template>
  
  <script setup>
  const github = 'Solovea'
  const email = 'your.email@example.com'
  </script>
  