# DebugPilot
 # AI Python Code Debugging Tutor
 A comprehensive system prompt designed to help AI assistants (like ChatGPT) provide educational debugging support for Python programming students. The prompt emphasizes guided discovery over direct solutions, fostering independent problem-solving skills.
 ##🎯 Purpose
This prompt transforms any AI assistant into an effective Python programming tutor that:
- Analyzes buggy Python code constructively
- Provides educational feedback through guided discovery
- Avoids giving away complete solutions
- Builds students\' debugging skills and confidence
- Adapts to different skill levels
- ## 🚀 Quick Start
Simply copy the content from [`ai-python-debugging-tutor-prompt.md`](./ai-python-debugging-tutor-prompt.md) and use it as a system prompt for your AI assistant of choice.
## 📋 What's Included
 **Main Prompt** (`ai-python-debugging-tutor-prompt.md`) - Complete system prompt ready to use
 **Sample Interactions** (`sample-interactions.md`) - Example conversations showing the prompt in action      **Adaptation Guide** (`adaptation-guide.md`) - How to customize for different contexts
 **Design Rationale** (`design-rationale.md`) - Detailed explanation of design choices
## 🎓 Key Features
### Educational Approach
 **Socratic Method**: Uses leading questions to guide students to solutions
 **Conceptual Learning**: Focuses on understanding rather than memorization
 **Progressive Hints**: Provides increasingly specific guidance without revealing answers
 **Skill Building**: Teaches transferable debugging strategies 
 ### Student-Friendly Design
  **Positive Reinforcement**: Always acknowledges what students did correctly
  **Adaptive Language**: Adjusts complexity based on student level
  **Emotional Support**: Handles frustration with empathy and encouragement
  **Growth Mindset**: Frames mistakes as learning opportunities
 ### Technical Coverage
  **All Error Types**: Syntax, logic, and runtime errors
  **Debugging Strategies**: Print statements, trace execution, error message analysis
  **Best Practices**: Code readability, efficiency, and structure
  **Comprehensive Scope**: Works across different Python topics and complexity levels
 ## 📊 Sample Interaction
 **Student's Buggy Code:**
 '''python
 def calculate_average(numbers):
 total = 0
 for i in range(numbers):      
   total += numbers[i]
  return total / len(numbers)
scores = [85, 92, 78, 96, 88]
print(calculate_average(scores))
'''
**AI Tutor Response (using our prompt):**
>I can see you're working on calculating an average - that's a fundamental and important skill! Your overall structure looks good, and I like how you're using a for loop and keeping track of the total.
> I notice something interesting in your for loop on line 3. Take a look at `range(numbers)` - what do you think Python is expecting `numbers` to be when it's used with `range()`?
> Here's a hint: think about what type of value `range()` typically works with, and what type of value you're actually passing to your function.
> Try running your code and see what error message you get - Python's error messages often give us great clues about what's going wrong!"
 
 ## 🛠️ Customization
 
 The prompt can be easily adapted for:
 **Different Programming Languages**: Modify language-specific examples and concepts
 **Specific Topics**: Focus on particular areas like data structures, algorithms, etc.
 **Age Groups**: Adjust language complexity and examples
 **Learning Environments**: Classroom, online courses, coding bootcamps, etc.
 See [`adaptation-guide.md`](./adaptation-guide.md) for detailed customization instructions.
 ## 📈 Effectiveness Principles
 ### Why This Approach Works
 1. **Active Learning**: Students discover solutions themselves, leading to better retention
 2. **Metacognition**: Develops awareness of thinking processes and problem-solving strategies
 3. **Confidence Building**: Success through guided discovery builds self-efficacy
 4. **Transfer**: Skills learned through questioning transfer to new problems
 5. **Engagement**: Interactive approach maintains student interest and motivation
 ### Research-Backed Techniques
 **Socratic Questioning**: Proven effective in computer science education
 **Zone of Proximal Development**: Provides appropriate level of challenge with support
 **Growth Mindset**: Emphasizes process over innate ability
 **Scaffolding**: Gradually reduces support as competence increases
 ## 🎯 Use Cases
 ### Educational Institutions
 **Computer Science Courses**: Supplement instructor feedback
 **Online Learning Platforms**: Provide 24/7 tutoring support
 **Coding Bootcamps**: Scale personalized feedback
 **Self-Study Programs**: Guide independent learners
 ### Development Teams
 **Code Review Training**: Teach junior developers debugging skills
 **Onboarding**: Help new team members learn codebase patterns
 **Mentorship Programs**: Structure mentoring conversations
 ## 🤝 Contributing
 We welcome contributions to improve the prompt! Please see our contribution guidelines:
 1. **Test Changes**: Validate any modifications with sample code scenarios
 2. **Maintain Balance**: Ensure changes preserve the educational vs. solution-giving balance
 3.**Document Rationale**: Explain the reasoning behind proposed changes
 4. **Provide Examples**: Include sample interactions demonstrating improvements
 ## 📄 License
 This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
 ## 🙏 Acknowledgments
 Inspired by effective computer science pedagogy research
 Built on principles of constructivist learning theory
 Designed with input from programming educators and students
 ## 📞 Support
For questions, suggestions, or issues:
Open an issue in this repository
Contribute improvements via pull requests
Share your experiences and adaptations
---
**Ready to transform AI assistance into AI tutoring? Start with our prompt and help students become independent problem-solvers!**'


