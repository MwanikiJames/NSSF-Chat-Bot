<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ask Me Anything</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        .question-bubble {
            border-radius: 18px 18px 18px 0;
        }
        .answer-bubble {
            border-radius: 18px 18px 0 18px;
        }
        .chat-container {
            height: 60vh;
            scrollbar-width: thin;
            scrollbar-color: #4f46e5 #e5e7eb;
        }
        .chat-container::-webkit-scrollbar {
            width: 8px;
        }
        .chat-container::-webkit-scrollbar-track {
            background: #e5e7eb;
        }
        .chat-container::-webkit-scrollbar-thumb {
            background-color: #4f46e5;
            border-radius: 20px;
        }
    </style>
</head>
<body class="gradient-bg min-h-screen">
    <div class="container mx-auto px-4 py-12">
        <div class="max-w-4xl mx-auto">
            <!-- Header -->
            <header class="text-center mb-12" data-aos="fade-down">
                <h1 class="text-4xl md:text-5xl font-bold text-indigo-800 mb-4">Ask Me Anything</h1>
                <p class="text-lg text-gray-600 max-w-2xl mx-auto">
                    Submit your questions and get answers directly on WhatsApp
                </p>
                <div class="mt-6 flex justify-center">
                    <div class="flex items-center bg-indigo-100 px-4 py-2 rounded-full">
                        <i data-feather="phone" class="text-indigo-600 mr-2"></i>
                        <span class="text-indigo-700 font-medium">0719595025</span>
                    </div>
                </div>
            </header>

            <!-- Chat Interface -->
            <div class="bg-white rounded-2xl shadow-xl overflow-hidden" data-aos="zoom-in">
                <!-- Chat Header -->
                <div class="bg-indigo-600 px-6 py-4 flex items-center">
                    <div class="w-10 h-10 rounded-full bg-indigo-500 flex items-center justify-center">
                        <i data-feather="message-square" class="text-white"></i>
                    </div>
                    <div class="ml-4">
                        <h3 class="text-white font-semibold">Q&A Chat</h3>
                        <p class="text-indigo-200 text-sm">Questions will be answered via WhatsApp</p>
                    </div>
                </div>

                <!-- Chat Messages -->
                <div class="chat-container overflow-y-auto p-6 space-y-4" id="chatMessages">
                    <!-- Welcome message -->
                    <div class="flex justify-start">
                        <div class="bg-indigo-100 question-bubble px-4 py-3 max-w-xs md:max-w-md">
                            <p class="text-gray-800">Hi there! Ask me anything and I'll reply via WhatsApp.</p>
                        </div>
                    </div>
                    <!-- Sample question/answer -->
                    <div class="flex justify-end">
                        <div class="bg-indigo-600 text-white answer-bubble px-4 py-3 max-w-xs md:max-w-md">
                            <p>How does this work?</p>
                        </div>
                    </div>
                    <div class="flex justify-start">
                        <div class="bg-indigo-100 question-bubble px-4 py-3 max-w-xs md:max-w-md">
                            <p class="text-gray-800">You ask a question here, I receive it on WhatsApp (0719595025), and reply there. The answer will appear here!</p>
                        </div>
                    </div>
                </div>

                <!-- Input Form -->
                <div class="border-t border-gray-200 p-4 bg-gray-50">
                    <form id="questionForm" class="flex space-x-2">
                        <input 
                            type="text" 
                            id="questionInput" 
                            placeholder="Type your question..." 
                            class="flex-1 px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:border-transparent"
                            required
                        >
                        <button 
                            type="submit" 
                            class="bg-indigo-600 hover:bg-indigo-700 text-white px-6 py-3 rounded-lg font-medium transition duration-200 flex items-center"
                        >
                            <span>Send</span>
                            <i data-feather="send" class="ml-2 w-4 h-4"></i>
                        </button>
                    </form>
                    <p class="text-xs text-gray-500 mt-2 text-center">By submitting, you agree to receive answers via WhatsApp</p>
                </div>
            </div>

            <!-- How it works section -->
            <div class="mt-16 grid md:grid-cols-3 gap-8" data-aos="fade-up">
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <div class="w-12 h-12 bg-indigo-100 rounded-full flex items-center justify-center mb-4">
                        <i data-feather="edit" class="text-indigo-600"></i>
                    </div>
                    <h3 class="font-semibold text-lg mb-2">1. Ask Your Question</h3>
                    <p class="text-gray-600">Type your question in the chat box above and submit it.</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <div class="w-12 h-12 bg-indigo-100 rounded-full flex items-center justify-center mb-4">
                        <i data-feather="smartphone" class="text-indigo-600"></i>
                    </div>
                    <h3 class="font-semibold text-lg mb-2">2. Sent to WhatsApp</h3>
                    <p class="text-gray-600">Your question is forwarded to our WhatsApp number 0719595025.</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md">
                    <div class="w-12 h-12 bg-indigo-100 rounded-full flex items-center justify-center mb-4">
                        <i data-feather="message-circle" class="text-indigo-600"></i>
                    </div>
                    <h3 class="font-semibold text-lg mb-2">3. Get Your Answer</h3>
                    <p class="text-gray-600">We reply on WhatsApp and the answer appears here in the chat.</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Initialize animations and icons
        AOS.init({
            duration: 800,
            once: true
        });
        feather.replace();

        // Form submission handler
        document.getElementById('questionForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const questionInput = document.getElementById('questionInput');
            const question = questionInput.value.trim();
            
            if (question) {
                // Add question to chat
                addMessageToChat(question, 'user');
                
                // Here you would normally send to your server/WhatsApp API
                // For demo, we'll simulate a response after 3 seconds
                setTimeout(() => {
                    addMessageToChat("Thanks for your question! I've received it on WhatsApp (0719595025) and will reply there shortly. The answer will appear here when I respond.", 'bot');
                }, 1500);
                
                // Clear input
                questionInput.value = '';
                
                // Scroll to bottom of chat
                const chatContainer = document.getElementById('chatMessages');
                chatContainer.scrollTop = chatContainer.scrollHeight;
            }
        });

        function addMessageToChat(message, sender) {
            const chatContainer = document.getElementById('chatMessages');
            const messageDiv = document.createElement('div');
            messageDiv.className = `flex ${sender === 'user' ? 'justify-end' : 'justify-start'}`;
            
            const bubble = document.createElement('div');
            bubble.className = sender === 'user' 
                ? 'bg-indigo-600 text-white answer-bubble px-4 py-3 max-w-xs md:max-w-md' 
                : 'bg-indigo-100 question-bubble px-4 py-3 max-w-xs md:max-w-md';
            bubble.textContent = message;
            
            messageDiv.appendChild(bubble);
            chatContainer.appendChild(messageDiv);
            
            // Scroll to new message
            chatContainer.scrollTop = chatContainer.scrollHeight;
        }
    </script>
</body>
</html>
