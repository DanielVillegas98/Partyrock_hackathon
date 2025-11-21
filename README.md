# Partyrock_hackathon
Json file for hackathon


{
    "widgets": [
        {
            "type": "static-text",
            "title": "Introduction",
            "content": "Welcome to the Medical Research Assistant. This tool helps medical professionals discover and share the latest research in their field. Select your specialty below to get started.",
            "x": 0,
            "y": 0,
            "width": 12,
            "height": 3
        },
        {
            "type": "select",
            "title": "Specialty Selection",
            "placeholder": "Select your medical specialty",
            "options": [
                "Orthopedics",
                "Ophthalmology",
                "Cardiology",
                "Neurology",
                "Dermatology",
                "Psychiatry",
                "Gastroenterology",
                "Pulmonology",
                "Rheumatology",
                "MedTech",
                "Biomedical Engineer"
            ],
            "defaultValue": null,
            "x": 0,
            "y": 3,
            "width": 12,
            "height": 2
        },
        {
            "type": "static-text",
            "title": "Research Request Instructions",
            "content": "Click below to generate summaries of the latest research articles in your field. The AI will create detailed summaries of 2-3 recent publications from top medical journals.\n\n",
            "x": 0,
            "y": 5,
            "width": 12,
            "height": 3
        },
        {
            "x": 0,
            "y": 8,
            "type": "inferred-text",
            "title": "Research Summaries",
            "width": 12,
            "height": 12,
            "prompt": "You are an expert medical research assistant helping a [Specialty Selection] specialist stay updated with recent literature. Generate a list of 5 recent, realistic research topics in {{Specialization Input}} that would appear in major medical journals like The Lancet, NEJM, JAMA, or specialty-specific journals in the last 3 months. For EACH topic, provide: 1. **Article Title**: Create a realistic journal article title 2. **Journal & Date**:Name a real journal + recent month/year\n3. **Key Findings** (2-3 sentences): Summarize the main clinical takeaway in clear, professional medical language \n4. **Clinical Impact**: One sentence on how this might change practice \n5. Read full article: (Include a placeholder link format) Format each article clearly with headers. Make the content scientifically accurate and clinically relevant to current [Specialty Selection] practice.",
            "parameters": {
                "model": "bedrock-anthropic.claude-3-5-sonnet-v2-0",
                "temperature": 0
            }
        },
        {
            "type": "static-text",
            "title": "Sharing Instructions",
            "content": "Enter the number (1, 2, 3, 4, or 5) of the article you'd like to share from above:",
            "x": 0,
            "y": 20,
            "width": 12,
            "height": 3
        },
        {
            "type": "select",
            "title": "Selected Article",
            "placeholder": "Select an article to share",
            "options": [
                "Article 1",
                "Article 2",
                "Article 3",
                "Article 4",
                "Article 5"
            ],
            "defaultValue": null,
            "x": 0,
            "y": 23,
            "width": 12,
            "height": 2
        },
        {
            "x": 0,
            "y": 26,
            "type": "inferred-text",
            "title": "LinkedIn Post",
            "width": 12,
            "height": 8,
            "prompt": "You are a medical communications expert helping doctors share research on professional social networks. Based on this research summary:[Research Summaries], select the \n[Selected Article] Create a social media post: **LINKEDIN POST** (Professional tone, 150-200 words): - Start with a compelling hook about the clinical significance - Summarize key findings in accessible professional language - Include 1-2 practical implications for healthcare professionals - End with a question to engage colleagues - Add 3-5 relevant hashtags (e.g., #MedEd #[Specialty Selection] #EvidenceBasedMedicine)",
            "parameters": {
                "model": "bedrock-anthropic.claude-3-5-sonnet-v2-0",
                "temperature": 0
            }
        },
        {
            "x": 0,
            "y": 34,
            "type": "inferred-text",
            "title": "Twitter Post",
            "width": 12,
            "height": 4,
            "prompt": "\nYou are a medical communications expert helping doctors share research on professional social networks. Based on this [Research Summaries] select [Selected Article] and Create a social media post: \n**TWITTER/X POST** (Concise, 250 characters max): - Ultra-brief key finding - One clinical implication - 2-3 hashtags - Engaging and shareable tone Make both posts professional, evidence-based, and engaging for healthcare professionals.",
            "parameters": {
                "model": "bedrock-anthropic.claude-3-5-sonnet-v2-0",
                "temperature": 0
            }
        },
        {
            "x": 0,
            "y": 38,
            "type": "inferred-text",
            "title": "Patient Explanation Email",
            "width": 12,
            "height": 8,
            "prompt": "You are a compassionate doctor explaining medical research to your patients in simple, reassuring language. Based on this research: [Research Summaries] select [Specialty Selection] and Create a PATIENT-FRIENDLY POST (200-250 words) that: - Uses simple, everyday language (avoid medical jargon) - Explains WHAT the research found in terms patients can understand - Explains WHY it matters for their health - Provides reassurance and context (not alarming) - Includes a clear call-to-action (e.g., \"If you have questions about this, let's discuss at your next appointment\") - Uses an empathetic, warm tone - Avoids overwhelming technical details Format with short paragraphs and maybe include an emoji or two to make it friendly and approachable. Think: \"How would I explain this to my own family?\"",
            "parameters": {
                "model": "bedrock-anthropic.claude-3-5-sonnet-v2-0",
                "temperature": 0
            }
        }
    ]
}
