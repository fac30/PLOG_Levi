## Guidance
Answer the following questions considering the learning outcomes for
- [Week 010](https://learn.foundersandcoders.com/course/syllabus/developer/week10-project05-DOTNET-intro/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> This week I delved into the rabbit hole of VPC's and subnets. MY aim was to include it for security purposes surrounding out database - but also to have my backend instance in the public subnet in the same VPC .
> 
> Here is an example of a PR I made for the project:
> 
> <img width="969" alt="Screenshot 2024-11-19 at 12 37 29" src="https://github.com/user-attachments/assets/d995e1ef-0574-4321-bdb0-97bce4afa053">
>
> However in deeper research, I found out that security groups are actually set for the instances/subnets and not the VPC. VPC's are automatically generated when you create an instance.  

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> With AWS, there are a lot of unnecessary costs. I wanted to create the subnets and deploy the backend and database this way. However where I found out that you'll need something called a NAT gateway is expensive - which essentially allows the private subnet within the VPC to communicate with the public - i also had to restart and therefore strip all of these resources back in my Terraform code.



## Feedback (For CF's)
> [**Course Facilitator name**]

Alexander

> [*What went well*]

Good research into AWS networking concepts, showing understanding of VPC, subnets, and security groups relationships. Practical learning about cost implications of AWS architecture decisions.

> [*Even better if*]

Show your Terraform code, even the version you had to strip back. Include specific configurations you tried for VPC and security groups since you mentioned working with them.
