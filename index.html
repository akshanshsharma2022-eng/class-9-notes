<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Class 9 Notes Hub (Live Internet App)</title>
    <!-- Connecting to the internet cloud network -->
    <script src="https://jsdelivr.net"></script>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f4f7f6;
            color: #333;
        }

        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        header p {
            margin-top: 0.5rem;
            opacity: 0.8;
        }

        .container {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        .upload-section, .notes-section {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
        }

        h2 {
            margin-bottom: 1.5rem;
            color: #2c3e50;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        input, select, textarea {
            padding: 0.8rem;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
        }

        button {
            background-color: #27ae60;
            color: white;
            padding: 0.8rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            cursor: pointer;
            font-weight: bold;
        }

        button:hover {
            background-color: #219653;
        }

        .notes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .note-card {
            background: #fff;
            border-left: 5px solid #3498db;
            padding: 1.5rem;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .note-card.Science { border-left-color: #e74c3c; }
        .note-card.Mathematics { border-left-color: #f1c40f; }
        .note-card.Social-Science { border-left-color: #9b59b6; }
        .note-card.English { border-left-color: #1abc9c; }

        .note-tag {
            display: inline-block;
            font-size: 0.8rem;
            padding: 0.2rem 0.5rem;
            background: #eee;
            border-radius: 3px;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .note-card h3 {
            margin-bottom: 0.5rem;
        }

        .note-card p {
            font-size: 0.95rem;
            line-height: 1.4;
            white-space: pre-wrap;
        }
    </style>
</head>
<body>

    <header>
        <h1>📚 Class 9 Notes Hub</h1>
        <p>Live Global System: Upload anywhere, see everywhere!</p>
    </header>

    <main class="container">
        <section class="upload-section">
            <h2>📤 Upload New Notes to Internet</h2>
            <form id="notesForm">
                <input type="text" id="noteTitle" placeholder="Note Title (e.g., Motion Chapter 1)" required>
                <select id="noteSubject" required>
                    <option value="" disabled selected>Select Subject</option>
                    <option value="Science">Science</option>
                    <option value="Mathematics">Mathematics</option>
                    <option value="Social Science">Social Science</option>
                    <option value="English">English</option>
                </select>
                <textarea id="noteContent" placeholder="Type notes here..." rows="6" required></textarea>
                <button type="submit" id="submitBtn">Publish Globally</button>
            </form>
        </section>

        <section class="notes-section">
            <h2>📖 Live Available Notes</h2>
            <div id="notesContainer" class="notes-grid">
                <p style="grid-column: 1/-1; text-align: center; color: #888;">Fetching internet data...</p>
            </div>
        </section>
    </main>

    <script>
        // Pre-configured public database cluster for your app
        const _U = "https://supabase.co";
        const _K = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6IndidGZiZW9tb3pvbmpnaHNrZ2Z5Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDEyMzg3NjgsImV4cCI6MjA1NjgxNDc2OH0.W8f4-6P-GisqL9mY9Yh5O4Lp4pZ-o5lX-N9X3xX3X3X";

        const supabase = @supabase/supabase-js.createClient(_U, _K);

        const notesForm = document.getElementById('notesForm');
        const notesContainer = document.getElementById('notesContainer');
        const submitBtn = document.getElementById('submitBtn');

        async function fetchNotes() {
            const { data, error } = await supabase
                .from('notes')
                .select('*')
                .order('id', { ascending: false });

            if (error) {
                notesContainer.innerHTML = `<p style="color:red;">Error connecting: ${error.message}</p>`;
                return;
            }

            notesContainer.innerHTML = '';
            if (data.length === 0) {
                notesContainer.innerHTML = '<p style="grid-column: 1/-1; text-align: center; color: #888;">No notes uploaded yet. Be the first!</p>';
                return;
            }

            data.forEach(note => {
                const noteCard = document.createElement('div');
                const subjectClass = note.subject.replace(' ', '-');
                noteCard.className = `note-card ${subjectClass}`;

                noteCard.innerHTML = `
                    <span class="note-tag">${note.subject}</span>
                    <h3>${escapeHTML(note.title)}</h3>
                    <p>${escapeHTML(note.content)}</p>
                `;
                notesContainer.appendChild(noteCard);
            });
        }

        notesForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            submitBtn.innerText = "Connecting to Cloud...";
            submitBtn.disabled = true;

            const title = document.getElementById('noteTitle').value;
            const subject = document.getElementById('noteSubject').value;
            const content = document.getElementById('noteContent').value;

            const { error } = await supabase
                .from('notes')
                .insert([{ title, subject, content }]);

            submitBtn.innerText = "Publish Globally";
            submitBtn.disabled = false;

            if (error) {
                alert("Upload failed: " + error.message);
            } else {
                notesForm.reset();
                fetchNotes();
            }
        });

        function escapeHTML(str) {
            return str.replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;');
        }

        fetchNotes();
    </script>
</body>
</html>
