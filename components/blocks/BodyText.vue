<template>
  <div>
    <TextBlock title="I'm Elijah Kelly." :text-on-right="false" image-url="corsairHydroX.jpg" :border-bottom="true">
      <p>I am a current student of computer science at Missouri University of Science and Technology. I think learning new things is fun, especially when it comes to software. I spend most of my free time coding things I think are cool. I also enjoy building computers when I can get my hands on parts!</p>
    </TextBlock>
    <TextBlock title="Education" :text-on-right="true" image-url="corsairHydroX.jpg" :border-bottom="true">
      <p>I'm a Junior at Missouri University of Science and Technology. I have earned a 3.3 GPA in the two years I've been on campus. Since starting the computer science program. Every semester I look to gain more knowledge both in and out of the classroom through personal projects.</p>
      <p>Coursework:</p>
      <ul class="list ml-5">
        <li>Data Structures</li>
        <li>Algorithms</li>
        <li>Theory of Computer Science</li>
        <li>Intro to Microcontrollers</li>
        <li>Software Engineering (In Progress)</li>
        <li>Operating Systems (In Progress)</li>
      </ul>
    </TextBlock>
    <TextBlock title="Experience" :text-on-right="false" image-url="corsairHydroX.jpg" :border-bottom="false">
      <p>I started at World Wide Technology in May 2019 as a JavaScript Intern. I work as part of the team responsable for the company's <a href="http://www.wwt.com" class="link text-blue-dark">new corporate website</a>. As a member of the team, I drastically improved on my skills as a developer. I learned to write quality, peer-reviewed, production level code to contribute to the project. During my summer at World Wide Technology, I grew as a team member as well. I presented contributions at weekly developer meetings and was entrusted to complete code reviews through GitHub. This position has vastly helped me gain skills in JavaScript, HTML & CSS, and being an effective member of a team.</p>
    </TextBlock>
    <TextBlock title="" :text-on-right="true" image-url="corsairHydroX.jpg" :border-bottom="true">
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
  background-color: rgba(36,123,160,.4);
}
.link:hover {
  background-color: rgba(6, 60, 83, 0.4);
}
.list {
  list-style-type: circle;
}
</style>