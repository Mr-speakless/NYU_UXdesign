# AI Filmmaking Collaboration and Asset Management
## Interview Records

---

# Participant 1: Henry

## Background and Recent Project

**Question: What is your role, and what do you usually do on a project?**

**Answer:** I am one of the main producers on the AI content team. I usually lead the organization and production of a project, although several people work on it. I help the team establish how the project will be made and what the production process will look like.

**Question: How does a project usually begin, and how is the work organized?**

**Answer:** We start with a kickoff process. My department leader coordinates with the producer. The producer, art director, post-production editor, our AI content department leader, and the client hold several meetings to refine the art treatment. Once the treatment is set, it is shared with our team. We review what our team is responsible for, what assets already exist, what the client will provide, and what we need to create. We also assess the scenes, shots, and difficulty, then build a timeline. We use a Notion table to list scenes, shots, camera movement, shot content, and each person's responsibility. Character designs are established in the art treatment, and we create the characters early so shot production can proceed.

## Shot Production and Review

**Question: Who defines the shots and decides whether they are complete?**

**Answer:** The script and shot count are generally planned by the art director, so those parts are relatively fixed. Our production team decides how to realize each shot and what the completion standard should be. We upload shots to Frame and invite the art director through a Slack group. The art director reviews the shots, marks which ones pass or need changes, and explains what should be adjusted. After editing, the client, our leader, and the producer also review the work.

**Question: Can you describe your recent process for generating a shot?**

**Answer:** We often start by using the Nano Banana Pro model in ComfyUI to generate high-quality still images. The still needs to meet the client's visual requirements—for example, a building may need to match the real building—and also fit our studio's aesthetic. Generating a good still can take 20 minutes, half an hour, or even an hour without a satisfactory result. More precise art direction makes it easier to get a good image quickly. We then use the Kling AI API for many generation attempts. We expand the art direction into prompts, sometimes with help from an AI skill, combine the prompts with the generated image, and see how the model performs.

**Question: How do you write and revise prompts?**

**Answer:** I usually ask AI to help with the broad prompt structure. We use a Claude skill because it understands our studio's aesthetic and organizes prompts around composition, camera angle, camera movement, lighting, and color atmosphere. I still review and adjust the result.

## Assets and Generation History

**Question: Where do you store project assets and how do you organize them?**

**Answer:** Most assets are stored locally. Naming is not very consistent: sometimes AI names files automatically, and sometimes we distinguish them manually. We usually use one folder per shot. Initial prompts, model weights and parameters, and many preparation assets are usually organized clearly, but details from fine-tuning a shot are often not preserved.

**Question: What happens when you need to find a successful result or recreate how it was made?**

**Answer:** A batch of experiments may combine three prompts with three reference images, creating nine possible combinations. Once we select a good result, we may hand off the batch of images and the batch of prompts, but it is not always clear which image and prompt combination produced the best result. We may also generate several batches of elements—for example, some images have a good scene while others have a good person—then combine those elements and generate again. Intermediate assets can get lost, or elements can change in the final image. Fixing the result may require generating the original elements again and repeating the adjustments.

## Collaboration and Handoffs

**Question: How do you share work and track what the team is doing?**

**Answer:** We communicate verbally and use Slack or Gmail to send files. We use Frame for review and a Notion table to track project status, completed work, and who may have time to help. However, team members have different project management habits, so it can be hard to see what everyone is working on. Our leader sometimes assigns tasks to people individually, and the rest of the team may not know whether someone is available or what projects they are handling.

**Question: What is difficult about receiving or handing off a shot?**

**Answer:** Most handoffs eventually get completed, but they can involve a lot of repeated work. Sometimes I receive a large package of source materials without seeing the earlier generation results. I have to test the materials again to understand what they produce, then figure out how to improve them. Prompts and reference images are the main things I need to retest.

## Challenges and Improvement Opportunities

**Question: Which production problems have the greatest impact on your work?**

**Answer:** It is difficult to trace which prompts, reference images, and settings produced a successful result. Intermediate assets can be lost during detailed adjustments, and handoffs do not always preserve the generation history. Finding the right combination again or rebuilding missing elements takes time and creates duplicate work.

**Question: How often do you need to retest existing work, and what do you do then?**

**Answer:** I estimate that this happens about once every four shots. Sometimes I decide it is easier to write a short prompt based on my own approach and then ask AI to improve it, because I understand my own creative direction better than I can infer it from an existing prompt.

**Question: What would you most like to improve about the team's process?**

**Answer:** I would like the team to communicate about projects more effectively. Each person may use a different project management approach, and those approaches are not shared consistently.

---

# Participant 2: Eddy

## Background and Recent Project

**Question: What is your role, and what work do you usually take on?**

**Answer:** I am a freelancer who joined the design studio for a short period to help with AI-generated content. I mainly support Henry with difficult shots, especially complex VFX compositing and post-production. I have a background in VFX and After Effects, and I have small tools of my own that help remove AI artifacts and make my work more efficient.

**Question: What project have you been working on recently?**

**Answer:** I have been helping wrap up a project called Edwards. It has several difficult shots that the art director has asked me to revise. One shot has a car entering the road from outside the frame, with pedestrians and a dog specified by the client, so it involves detailed compositing. Another is a very wide shot with tiny people. I generated parts separately with AI and assembled them into one image. Both tasks take a lot of time.

## Shot Production and Review

**Question: Who decides how shots are divided and assigned?**

**Answer:** The art director, our team leader, and Henry, the main person responsible for the generation project, usually make those decisions. I generally execute the assigned work. We share updates through Slack.

**Question: Can you describe how you handled the swimming pool shot?**

**Answer:** Henry gave me the original swimming pool clip, a frame image, a swimming pool image, and a video prompt. I divided the frame into four quadrants and generated a high-resolution frame for each section. I wrote prompts to make the people move slightly while keeping them inside their own section, so they would not cross a boundary and create a continuity problem. I then generated each section, composited them together, and rendered the combined result again. In After Effects, I added or adjusted effects such as the sky, color, gradients, and lens focal length. I thought the final result was good, although the process pushed the AI close to its limits.

**Question: How do you write prompts or get help with them?**

**Answer:** I generally write prompts myself and sometimes use AI. Henry has a prompt skill, but I do not find it comfortable to use, so I tend to use my own method. If I really need help, I will ask. Most of the time, if information or a prompt is not provided, I work it out myself rather than asking someone to send it.

## Assets and Generation History

**Question: How do you name and locate files?**

**Answer:** I use my own VFX naming conventions. I usually handle a batch of about 10 to 20 shots, so it is fairly easy for me to remember where those shots are. We also use a Notion document to manage the work. When I cannot find an asset, I ask in the group. If a colleague does not reply quickly, I may look in the Kling AI app or website, where some assets and prompts may be stored.

## Collaboration and Handoffs

**Question: How do you find out what other people are working on?**

**Answer:** I mainly use Notion to understand what people are handling, but it can be difficult to tell who is working on what. Usually, I ask directly. We share work through Slack.

**Question: What information did you receive when taking on the Edwards work?**

**Answer:** Henry gave me a package that could include the project overview, the art treatment, existing videos linked in Frame, images, and generation prompts. When the art director is unhappy with a specific part, I still have to open the Frame page and watch the video to understand exactly what needs to change.

## Challenges and Improvement Opportunities

**Question: What takes the most time or causes the most frustration?**

**Answer:** Generation and waiting are the most time-consuming parts. Something that seems like it should work may not work in practice, which is frustrating. It can affect the schedule; sometimes we adjust the timeline, and I may work overtime.

**Question: What would make it easier for you to take over a problem and solve it?**

**Answer:** Reducing communication overhead would help. I would like to understand more smoothly what problem the team is facing and where it is, so I can work on the issue directly instead of first having to diagnose it again myself.

---

# Participant 3: Jwan

## Background and Recent Project

**Question: What is your role, and how do you usually work with the team?**

**Answer:** I work with Henry on AI content and produce part of the project's AI imagery. Sometimes I complete my shots independently, and sometimes I work with the team. The team is usually three or four people.

**Question: How many shots are usually in a project, and what project have you worked on recently?**

**Answer:** A project usually has around 40 to 50 shots. Recently, I worked on a yacht film. The client wanted to show the yacht and the texture of the coast, sea, and rocks. We spent a lot of effort on the visual quality while also trying to reproduce the client's yacht design accurately.

## Shot Production and Review

**Question: How are the shots assigned and reviewed?**

**Answer:** The team divides the shots and assigns people to them. The project process is similar to the one Henry described: the art director, leader, producer, and client meet first, then the team receives the art treatment and divides up the work. Each person first decides whether their own shots meet the art treatment requirements, then uploads them to Frame for the art director to judge. Approved shots go to the editor. After editing, the client, leader, and producer review the cut and give feedback.

**Question: Which tools do you use, and how many generations does a shot usually take?**

**Answer:** I use Kling AI (heard in the interview as “Coling AI”), NanoPrompt, ChatGPT, and “Copy UI” (tool name uncertain; it may refer to ComfyUI). A shot often takes between 10 and 20 generation attempts.

**Question: How do you iterate on a shot?**

**Answer:** We work in batches. I combine a prompt with a reference image and generate a batch, often around five videos. If one works, I select it and upload it. If none work, I revise the prompt or approach and generate another batch, such as batch 2.

## Assets and Handoffs

**Question: How do you name and organize files?**

**Answer:** We name files by project and then use different names for each shot within the project. When assets are missing, there is usually no clear way to recover them. We mainly ask each other verbally.

**Question: How does the team track and hand off work?**

**Answer:** We use a Notion document to manage assignments, work content, and handoffs. We use Slack to pass handoff information.

## Challenges and Improvement Opportunities

**Question: What is difficult about getting feedback on your work?**

**Answer:** It can be difficult when the work does not meet the leader's expectations. We may report progress at most once a day because generating content takes time. If I spend the day working and the leader is not satisfied at the next review, it can feel as if that day's work was wasted.

**Question: What would help you avoid late feedback and unnecessary work?**

**Answer:** I would like the leader to have a clearer view of our progress. Sometimes a still image is enough to judge whether a visual direction is good or bad, but we may wait until it has become a video of around ten seconds before showing it. Then we may learn only at that point that the leader does not approve. Earlier feedback on stills could help us decide whether to continue before spending time generating the full video.

---

## Notes on Unconfirmed Details

- Eddy's name was provided as “Eddy,” with the letter spelling “E-D-I”; confirm the preferred written name.
- Jwan's background was described as being from Spain; nationality and current location were not confirmed.
- Jwan's tool names “NanoPrompt” and “Copy UI,” and the spoken name “Coling AI,” may need confirmation.
- Jwan's account included an unclear reference to the person assigning shots; the name and role were not clear, so it is not attributed to Jwan.
