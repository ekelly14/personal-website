<template>
  <div>
    <TextBlock title="I'm Elijah Kelly" :text-on-right="false" image-url="personal_image.jpg" :border-bottom="true" :round-image="true">
      <p>I am a current student of computer science at Missouri University of Science and Technology. I think learning new things is fun, especially when it comes to software. I spend most of my free time coding things I think are cool. I also enjoy building computers when I can get my hands on parts!</p>
    </TextBlock>
    <TextBlock title="Education" :text-on-right="true" image-url="school.png" :border-bottom="true">
      <p>I'm a Junior at Missouri University of Science and Technology. I have earned a 3.3 GPA in the two years I've been on campus. Since starting the computer science program, I have gained a lot of technical and intrapersonal skills. Every semester I look to gain more knowledge both in and out of the classroom through personal projects.</p>
      <p class="bold">Coursework:</p>
      <ul class="list ml-5">
        <li>Data Structures</li>
        <li>Algorithms</li>
        <li>Theory of Computer Science</li>
        <li>Intro to Microcontrollers</li>
        <li>Software Engineering (In Progress)</li>
        <li>Operating Systems (In Progress)</li>
      </ul>
    </TextBlock>
    <TextBlock title="Skills & Involvement" :text-on-right="false" image-url="laptop.jpg" :border-bottom="false">
      <ul class="list ml-5">
        <li>C++ -- Proficient</li>
        <li>JavaScript -- Proficient</li>
        <li>Python -- Proficient</li>
        <li>CSS3 -- Growing Skill</li>
        <li>Data Structures</li>
        <li>Algorithms</li>
      </ul>
      <p>I have many intrapersonal skills in addition to technical skills. I have experience working as part of a team from both my internship and many school projects.</p>
    </TextBlock>
    <TextBlock :text-on-right="true" image-url="eagle.jpg" :border-bottom="true">
      <p>One way I have learned to build my interpersonal skills is on my journey to Eagle Scout. In completing my <a href="https://en.wikipedia.org/wiki/Eagle_Scout_Service_Project" class="link text-blue-dark">Eagle Scout Project</a>, I learned to plan and effectively implement a bridge for a nature trail at an elementary school. As part of effectively implementing the project, I had to learn how to be able to lead and communicate with the people helping me.</p>
    </TextBlock>
    <TextBlock title="Experience" :text-on-right="false" image-url="wwt.jpg" :border-bottom="false">
      <p>I started at World Wide Technology in May 2019 as a JavaScript Intern. I work as part of the team responsable for the company's <a href="http://www.wwt.com" class="link text-blue-dark">new corporate website</a>. As a member of the team, I drastically improved on my skills as a developer. I learned to write quality, peer-reviewed, production level code to contribute to the project. During my summer at World Wide Technology, I grew as a team member as well. I presented contributions at weekly developer meetings and was entrusted to complete code reviews through GitHub. This position has vastly helped me gain skills in JavaScript, HTML & CSS, and being an effective member of a team.</p>
    </TextBlock>
    <TextBlock title="" :text-on-right="true" image-url="mst_cs.png" :border-bottom="true">
      <p>I have also worked as a student grader in the computer science department at Missouri S&T. After seeing my performance in Intro to Programming class, my professor hand selected me for the position. As part of the job, I evaluated other student's work, assigned grades, and gave constructive feedback to new and experienced programmers. I was chosen for this position because I excelled in class and have an above average knowledge of the course material.</p>
    </TextBlock>
  </div>
</template>

<script>
import TextBlock from '~/components/general/TextBlock.vue'
  export default {
    name: 'BodyText',
    components: {
      TextBlock
    }
  }
</script>

<style scoped>
.link {
  background-color: rgba(36,123,160,.2);
}
.link:hover {
  background-color: rgba(120, 193, 224, 0.2);
}
.list {
  list-style-type: circle;
}
.list > li {
  font-style: italic;
}
</style>