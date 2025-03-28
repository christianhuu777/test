<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Musée Vivant de la Vigne et du Cognac | Partagez Vos Histoires et Souvenirs</title>
    <meta name="description" content="Partagez vos histoires familiales, souvenirs et expériences avec le Musée Vivant de la Vigne et du Cognac. Contribuez à notre patrimoine vivant.">
    <link rel="canonical" href="https://musee-vigne-cognac.fr/partage-vos-histoires">
    <style>
        :root {
            --primary: #5a2d0c;
            --secondary: #c19a6b;
            --accent: #8b0000;
            --light: #f8f1e5;
            --dark: #2c1e0f;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Georgia', serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1474722883778-792e7990302f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 4rem 1rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .theme-selector {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
            justify-content: center;
        }
        
        .theme-btn {
            padding: 10px 20px;
            background-color: var(--secondary);
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: bold;
        }
        
        .theme-btn:hover, .theme-btn.active {
            background-color: var(--accent);
            color: white;
        }
        
        .ugc-form {
            background-color: white;
            border-radius: 8px;
            padding: 30px;
            margin: 30px auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-width: 800px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        
        input[type="text"], textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        .upload-area {
            border: 2px dashed var(--secondary);
            border-radius: 8px;
            padding: 30px;
            text-align: center;
            cursor: pointer;
            margin: 20px 0;
            transition: all 0.3s;
        }
        
        .upload-area:hover {
            border-color: var(--accent);
            background-color: rgba(193, 154, 107, 0.1);
        }
        
        .upload-icon {
            font-size: 40px;
            color: var(--secondary);
            margin-bottom: 10px;
        }
        
        .submit-btn {
            background-color: var(--accent);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 18px;
            transition: background-color 0.3s;
            display: block;
            margin: 30px auto 0;
            width: 200px;
            text-align: center;
        }
        
        .submit-btn:hover {
            background-color: #6d0000;
        }
        
        .preview-image {
            max-width: 100%;
            max-height: 300px;
            margin-top: 20px;
            border-radius: 4px;
            display: none;
        }
        
        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 50px;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .subtitle {
                font-size: 1rem;
            }
            
            .theme-btn {
                padding: 8px 15px;
                font-size: 14px;
            }
            
            .ugc-form {
                padding: 20px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <h1>Partagez Vos Histoires de Vigne</h1>
            <p class="subtitle">Contribuez à la mémoire vivante du Musée Vivant de la Vigne et du Cognac</p>
        </div>
    </header>
    
    <div class="container">
        <div class="theme-selector">
            <button class="theme-btn active" data-theme="family">Histoires Familiales</button>
            <button class="theme-btn" data-theme="folklore">Folklore de la Vigne</button>
            <button class="theme-btn" data-theme="festivals">Fêtes & Événements</button>
            <button class="theme-btn" data-theme="memories">Souvenirs Personnels</button>
        </div>
        
        <div class="ugc-form">
            <div class="form-group">
                <label for="name">Votre Nom</label>
                <input type="text" id="name" placeholder="Jean Dupont">
            </div>
            
            <div class="form-group">
                <label for="email">Email (facultatif)</label>
                <input type="text" id="email" placeholder="votre@email.com">
            </div>
            
            <div class="form-group">
                <label for="story-title">Titre de l'Histoire</label>
                <input type="text" id="story-title" placeholder="Le Vignoble de Mon Grand-Père">
            </div>
            
            <div class="form-group">
                <label for="story">Votre Histoire</label>
                <textarea id="story" placeholder="Partagez vos souvenirs, histoires ou traditions liées à la vigne et au cognac..."></textarea>
            </div>
            
            <div class="upload-area" id="uploadArea">
                <div class="upload-icon">
                    <i class="fas fa-camera"></i>
                </div>
                <p>Cliquez pour télécharger des photos ou glisser-déposer</p>
                <input type="file" id="imageUpload" accept="image/*" class="hidden" multiple>
            </div>
            
            <img id="previewImage" class="preview-image" alt="Aperçu">
            
            <button class="submit-btn" id="submitBtn">Soumettre</button>
        </div>
    </div>
    
    <footer>
        <div class="container">
            <p>Musée Vivant de la Vigne et du Cognac &copy; <span id="currentYear"></span> - <a href="https://musee-vigne-cognac.fr" style="color: white; text-decoration: underline;">musee-vigne-cognac.fr</a></p>
        </div>
    </footer>
    
    <script>
        // Mettre à jour l'année du copyright automatiquement
        document.getElementById('currentYear').textContent = new Date().getFullYear();
        
        document.addEventListener('DOMContentLoaded', function() {
            // Sélection du thème
            const themeBtns = document.querySelectorAll('.theme-btn');
            themeBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    themeBtns.forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Téléchargement d'image
            const uploadArea = document.getElementById('uploadArea');
            const imageUpload = document.getElementById('imageUpload');
            const previewImage = document.getElementById('previewImage');
            
            uploadArea.addEventListener('click', function() {
                imageUpload.click();
            });
            
            // Glisser-déposer
            uploadArea.addEventListener('dragover', function(e) {
                e.preventDefault();
                this.style.borderColor = 'var(--accent)';
                this.style.backgroundColor = 'rgba(139, 0, 0, 0.1)';
            });
            
            uploadArea.addEventListener('dragleave', function() {
                this.style.borderColor = 'var(--secondary)';
                this.style.backgroundColor = '';
            });
            
            uploadArea.addEventListener('drop', function(e) {
                e.preventDefault();
                this.style.borderColor = 'var(--secondary)';
                this.style.backgroundColor = '';
                
                if (e.dataTransfer.files.length) {
                    imageUpload.files = e.dataTransfer.files;
                    showPreview(imageUpload.files[0]);
                }
            });
            
            imageUpload.addEventListener('change', function() {
                if (this.files.length) {
                    showPreview(this.files[0]);
                }
            });
            
            function showPreview(file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    previewImage.src = e.target.result;
                    previewImage.style.display = 'block';
                };
                reader.readAsDataURL(file);
            }
            
            // Soumission du formulaire
            const submitBtn = document.getElementById('submitBtn');
            submitBtn.addEventListener('click', function() {
                const name = document.getElementById('name').value;
                const title = document.getElementById('story-title').value;
                const story = document.getElementById('story').value;
                const theme = document.querySelector('.theme-btn.active').dataset.theme;
                
                if (!name || !title || !story) {
                    alert('Veuillez remplir tous les champs obligatoires');
                    return;
                }
                
                // Ici vous enverriez normalement les données au serveur
                alert(`Merci pour votre soumission sur ${theme}! Votre histoire "${title}" a bien été reçue.`);
                
                // Réinitialisation du formulaire
                document.getElementById('name').value = '';
                document.getElementById('email').value = '';
                document.getElementById('story-title').value = '';
                document.getElementById('story').value = '';
                imageUpload.value = '';
                previewImage.style.display = 'none';
            });
        });
    </script>
</body>
</html>
