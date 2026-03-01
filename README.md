<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NGN OPTIC | Excellence en Optique Médicale</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        gold: {
                            400: '#D4AF37',
                            500: '#C5A028',
                            600: '#B8941F',
                        },
                        navy: {
                            800: '#1A1F3C',
                            900: '#0F1429',
                        }
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'fade-in-up': 'fadeInUp 0.8s ease-out forwards',
                        'spin-slow': 'spin 20s linear infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .glass-effect {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .text-gradient {
            background: linear-gradient(135deg, #D4AF37 0%, #F4E5C2 50%, #D4AF37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero-pattern {
            background-image: radial-gradient(circle at 1px 1px, rgba(212, 175, 55, 0.15) 1px, transparent 0);
            background-size: 40px 40px;
        }
        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }
        .scroll-reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
        .service-card:hover .service-icon {
            transform: scale(1.1) rotate(5deg);
        }
        .nav-link {
            position: relative;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 0;
            background-color: #D4AF37;
            transition: width 0.3s;
        }
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="font-sans bg-slate-50 text-slate-800 overflow-x-hidden">

    <!-- Navigation -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-300 bg-transparent">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 flex items-center gap-3">
                    <div class="w-10 h-10 bg-gradient-to-br from-gold-400 to-gold-600 rounded-full flex items-center justify-center shadow-lg">
                        <i class="fas fa-eye text-white text-lg"></i>
                    </div>
                    <span class="font-serif text-2xl font-bold text-white tracking-wide">NGN <span class="text-gold-400">OPTIC</span></span>
                </div>
                
                <div class="hidden md:flex space-x-8">
                    <a href="#accueil" class="nav-link text-white hover:text-gold-400 transition-colors text-sm font-medium uppercase tracking-wider">Accueil</a>
                    <a href="#services" class="nav-link text-white hover:text-gold-400 transition-colors text-sm font-medium uppercase tracking-wider">Services</a>
                    <a href="#produits" class="nav-link text-white hover:text-gold-400 transition-colors text-sm font-medium uppercase tracking-wider">Produits</a>
                    <a href="#about" class="nav-link text-white hover:text-gold-400 transition-colors text-sm font-medium uppercase tracking-wider">À Propos</a>
                    <a href="#contact" class="nav-link text-white hover:text-gold-400 transition-colors text-sm font-medium uppercase tracking-wider">Contact</a>
                </div>

                <div class="hidden md:flex items-center gap-4">
                    <a href="tel:+2290197488477" class="flex items-center gap-2 text-gold-400 hover:text-gold-300 transition-colors">
                        <i class="fas fa-phone-alt text-sm"></i>
                        <span class="text-sm font-semibold">+229 01 97 48 84 77</span>
                    </a>
                </div>

                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-white hover:text-gold-400">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-navy-900/95 backdrop-blur-lg absolute w-full border-t border-white/10">
            <div class="px-4 pt-2 pb-6 space-y-2">
                <a href="#accueil" class="block px-3 py-2 text-white hover:text-gold-400 hover:bg-white/5 rounded-md">Accueil</a>
                <a href="#services" class="block px-3 py-2 text-white hover:text-gold-400 hover:bg-white/5 rounded-md">Services</a>
                <a href="#produits" class="block px-3 py-2 text-white hover:text-gold-400 hover:bg-white/5 rounded-md">Produits</a>
                <a href="#about" class="block px-3 py-2 text-white hover:text-gold-400 hover:bg-white/5 rounded-md">À Propos</a>
                <a href="#contact" class="block px-3 py-2 text-white hover:text-gold-400 hover:bg-white/5 rounded-md">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="accueil" class="relative min-h-screen flex items-center justify-center overflow-hidden bg-navy-900">
        <div class="absolute inset-0 hero-pattern opacity-20"></div>
        
        <!-- Animated Background Elements -->
        <div class="absolute top-20 left-10 w-72 h-72 bg-gold-400/10 rounded-full blur-3xl animate-float"></div>
        <div class="absolute bottom-20 right-10 w-96 h-96 bg-blue-500/10 rounded-full blur-3xl animate-float" style="animation-delay: 2s;"></div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <div class="animate-fade-in-up">
                <p class="text-gold-400 font-medium tracking-[0.3em] uppercase mb-4 text-sm md:text-base">République du Bénin • Porto-Novo</p>
                <h1 class="font-serif text-5xl md:text-7xl lg:text-8xl font-bold text-white mb-6 leading-tight">
                    Votre Vision,<br>
                    <span class="text-gradient">Notre Passion</span>
                </h1>
                <p class="mt-4 max-w-2xl mx-auto text-xl text-slate-300 font-light leading-relaxed">
                    Expert en optique médicale et solaire. Verres sur ordonnance, tests de vue professionnels et livraison mondiale.
                </p>
                
                <div class="mt-10 flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#services" class="px-8 py-4 bg-gradient-to-r from-gold-400 to-gold-600 text-navy-900 font-semibold rounded-full hover:shadow-lg hover:shadow-gold-400/30 transition-all transform hover:-translate-y-1">
                        Découvrir Nos Services
                    </a>
                    <a href="https://wa.me/2290197488477" target="_blank" class="px-8 py-4 border-2 border-white/30 text-white font-semibold rounded-full hover:bg-white/10 transition-all flex items-center justify-center gap-2">
                        <i class="fab fa-whatsapp text-green-400"></i>
                        Prendre Rendez-vous
                    </a>
                </div>
            </div>

            <!-- Stats -->
            <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-8 border-t border-white/10 pt-10">
                <div class="text-center">
                    <div class="text-3xl font-bold text-gold-400 font-serif">10+</div>
                    <div class="text-slate-400 text-sm mt-1">Années d'expérience</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold text-gold-400 font-serif">5000+</div>
                    <div class="text-slate-400 text-sm mt-1">Clients satisfaits</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold text-gold-400 font-serif">50+</div>
                    <div class="text-slate-400 text-sm mt-1">Pays livrés</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold text-gold-400 font-serif">100%</div>
                    <div class="text-slate-400 text-sm mt-1">Sur mesure</div>
                </div>
            </div>
        </div>

        <!-- Scroll Indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
            <i class="fas fa-chevron-down text-gold-400 text-2xl"></i>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 bg-white relative overflow-hidden">
        <div class="absolute top-0 right-0 w-1/3 h-full bg-gradient-to-l from-slate-50 to-transparent"></div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 scroll-reveal">
                <h2 class="font-serif text-4xl md:text-5xl font-bold text-navy-900 mb-4">Nos Expertises</h2>
                <div class="w-24 h-1 bg-gold-400 mx-auto"></div>
                <p class="mt-4 text-slate-600 max-w-2xl mx-auto">Des solutions optiques complètes alliant technologie de pointe et savoir-faire artisanal</p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Service 1 -->
                <div class="service-card group p-8 bg-slate-50 rounded-2xl hover:bg-navy-900 transition-all duration-500 hover:shadow-2xl scroll-reveal">
                    <div class="service-icon w-16 h-16 bg-gold-400 rounded-2xl flex items-center justify-center mb-6 transition-transform duration-300 shadow-lg">
                        <i class="fas fa-prescription text-2xl text-navy-900"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-navy-900 group-hover:text-white mb-3 transition-colors">Verres Médicaux</h3>
                    <p class="text-slate-600 group-hover:text-slate-300 text-sm leading-relaxed transition-colors">
                        Réalisation sur ordonnance avec traitements anti-reflet, anti-rayures et verres progressifs haute définition.
                    </p>
                </div>

                <!-- Service 2 -->
                <div class="service-card group p-8 bg-slate-50 rounded-2xl hover:bg-navy-900 transition-all duration-500 hover:shadow-2xl scroll-reveal" style="transition-delay: 100ms;">
                    <div class="service-icon w-16 h-16 bg-gold-400 rounded-2xl flex items-center justify-center mb-6 transition-transform duration-300 shadow-lg">
                        <i class="fas fa-sun text-2xl text-navy-900"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-navy-900 group-hover:text-white mb-3 transition-colors">Verres Solaires</h3>
                    <p class="text-slate-600 group-hover:text-slate-300 text-sm leading-relaxed transition-colors">
                        Protection UV400 avec verres polarisés, photochromiques et teintes personnalisées sur mesure.
                    </p>
                </div>

                <!-- Service 3 -->
                <div class="service-card group p-8 bg-slate-50 rounded-2xl hover:bg-navy-900 transition-all duration-500 hover:shadow-2xl scroll-reveal" style="transition-delay: 200ms;">
                    <div class="service-icon w-16 h-16 bg-gold-400 rounded-2xl flex items-center justify-center mb-6 transition-transform duration-300 shadow-lg">
                        <i class="fas fa-eye text-2xl text-navy-900"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-navy-900 group-hover:text-white mb-3 transition-colors">Test de Vue</h3>
                    <p class="text-slate-600 group-hover:text-slate-300 text-sm leading-relaxed transition-colors">
                        Examen complet par optométriste diplômé avec équipement électronique de dernière génération.
                    </p>
                </div>

                <!-- Service 4 -->
                <div class="service-card group p-8 bg-slate-50 rounded-2xl hover:bg-navy-900 transition-all duration-500 hover:shadow-2xl scroll-reveal" style="transition-delay: 300ms;">
                    <div class="service-icon w-16 h-16 bg-gold-400 rounded-2xl flex items-center justify-center mb-6 transition-transform duration-300 shadow-lg">
                        <i class="fas fa-globe-africa text-2xl text-navy-900"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-navy-900 group-hover:text-white mb-3 transition-colors">Livraison Mondiale</h3>
                    <p class="text-slate-600 group-hover:text-slate-300 text-sm leading-relaxed transition-colors">
                        Expédition sécurisée dans le monde entier avec suivi en temps réel et emballage renforcé.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Showcase -->
    <section id="produits" class="py-24 bg-navy-900 relative">
        <div class="absolute inset-0 hero-pattern opacity-10"></div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-end mb-16 scroll-reveal">
                <div>
                    <h2 class="font-serif text-4xl md:text-5xl font-bold text-white mb-4">Nos Collections</h2>
                    <div class="w-24 h-1 bg-gold-400"></div>
                </div>
                <p class="text-slate-400 mt-4 md:mt-0 max-w-md">Des montures tendance et des verres d'exception pour sublimer votre regard</p>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <!-- Product 1 -->
                <div class="group relative overflow-hidden rounded-2xl bg-white/5 backdrop-blur-sm border border-white/10 hover:border-gold-400/50 transition-all duration-500 scroll-reveal">
                    <div class="aspect-[4/3] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1574258495973-f010dfbb5371?w=800&auto=format&fit=crop&q=80" alt="Lunettes médicales" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-serif text-xl font-bold text-white">Optique Médicale</h3>
                            <span class="text-gold-400 text-sm font-semibold">Sur mesure</span>
                        </div>
                        <p class="text-slate-400 text-sm mb-4">Montures designer et verres correcteurs haute précision</p>
                        <div class="flex gap-2">
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Progressifs</span>
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Anti-lumière bleue</span>
                        </div>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="group relative overflow-hidden rounded-2xl bg-white/5 backdrop-blur-sm border border-white/10 hover:border-gold-400/50 transition-all duration-500 scroll-reveal" style="transition-delay: 100ms;">
                    <div class="aspect-[4/3] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1511499767150-a48a237f0083?w=800&auto=format&fit=crop&q=80" alt="Lunettes solaires" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-serif text-xl font-bold text-white">Solaire Premium</h3>
                            <span class="text-gold-400 text-sm font-semibold">UV400</span>
                        </div>
                        <p class="text-slate-400 text-sm mb-4">Protection maximale avec style contemporain</p>
                        <div class="flex gap-2">
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Polarisés</span>
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Photochromiques</span>
                        </div>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="group relative overflow-hidden rounded-2xl bg-white/5 backdrop-blur-sm border border-white/10 hover:border-gold-400/50 transition-all duration-500 scroll-reveal" style="transition-delay: 200ms;">
                    <div class="aspect-[4/3] overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1572635196237-14b3f281503f?w=800&auto=format&fit=crop&q=80" alt="Accessoires" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="font-serif text-xl font-bold text-white">Accessoires</h3>
                            <span class="text-gold-400 text-sm font-semibold">Essentiels</span>
                        </div>
                        <p class="text-slate-400 text-sm mb-4">Étuis, sprays, tournevis et chaînes de lunettes</p>
                        <div class="flex gap-2">
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Cuir premium</span>
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs text-slate-300">Microfibre</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section class="py-24 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 scroll-reveal">
                <h2 class="font-serif text-4xl md:text-5xl font-bold text-navy-900 mb-4">Notre Processus</h2>
                <div class="w-24 h-1 bg-gold-400 mx-auto"></div>
            </div>

            <div class="relative">
                <!-- Connection Line -->
                <div class="hidden md:block absolute top-1/2 left-0 w-full h-0.5 bg-gold-200 -translate-y-1/2 z-0"></div>
                
                <div class="grid md:grid-cols-4 gap-8 relative z-10">
                    <div class="text-center scroll-reveal">
                        <div class="w-20 h-20 mx-auto bg-white rounded-full shadow-xl flex items-center justify-center border-4 border-gold-400 mb-4 relative">
                            <span class="text-2xl font-bold text-navy-900">1</span>
                            <div class="absolute -top-2 -right-2 w-6 h-6 bg-green-500 rounded-full flex items-center justify-center">
                                <i class="fas fa-check text-white text-xs"></i>
                            </div>
                        </div>
                        <h3 class="font-serif text-lg font-bold text-navy-900 mb-2">Consultation</h3>
                        <p class="text-slate-600 text-sm">Examen de la vue complet et conseil personnalisé</p>
                    </div>

                    <div class="text-center scroll-reveal" style="transition-delay: 100ms;">
                        <div class="w-20 h-20 mx-auto bg-white rounded-full shadow-xl flex items-center justify-center border-4 border-gold-400 mb-4 relative">
                            <span class="text-2xl font-bold text-navy-900">2</span>
                        </div>
                        <h3 class="font-serif text-lg font-bold text-navy-900 mb-2">Choix des Verres</h3>
                        <p class="text-slate-600 text-sm">Sélection des matériaux et traitements adaptés</p>
                    </div>

                    <div class="text-center scroll-reveal" style="transition-delay: 200ms;">
                        <div class="w-20 h-20 mx-auto bg-white rounded-full shadow-xl flex items-center justify-center border-4 border-gold-400 mb-4 relative">
                            <span class="text-2xl font-bold text-navy-900">3</span>
                        </div>
                        <h3 class="font-serif text-lg font-bold text-navy-900 mb-2">Fabrication</h3>
                        <p class="text-slate-600 text-sm">Taillage et montage par nos opticiens experts</p>
                    </div>

                    <div class="text-center scroll-reveal" style="transition-delay: 300ms;">
                        <div class="w-20 h-20 mx-auto bg-white rounded-full shadow-xl flex items-center justify-center border-4 border-gold-400 mb-4 relative">
                            <span class="text-2xl font-bold text-navy-900">4</span>
                        </div>
                        <h3 class="font-serif text-lg font-bold text-navy-900 mb-2">Livraison</h3>
                        <p class="text-slate-600 text-sm">Remise en main propre ou expédition internationale</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div class="scroll-reveal">
                    <div class="relative">
                        <div class="absolute -top-4 -left-4 w-24 h-24 bg-gold-400/20 rounded-full"></div>
                        <div class="absolute -bottom-4 -right-4 w-32 h-32 bg-navy-900/10 rounded-full"></div>
                        <img src="https://images.unsplash.com/photo-1582139329536-e7284fece509?w=800&auto=format&fit=crop&q=80" alt="Atelier NGN Optic" class="relative rounded-2xl shadow-2xl w-full">
                        <div class="absolute -bottom-6 -right-6 bg-navy-900 text-white p-6 rounded-xl shadow-xl">
                            <div class="text-3xl font-bold text-gold-400 font-serif">Depuis</div>
                            <div class="text-4xl font-bold">2014</div>
                        </div>
                    </div>
                </div>

                <div class="scroll-reveal">
                    <h2 class="font-serif text-4xl md:text-5xl font-bold text-navy-900 mb-6">L'Excellence Béninoise à l'International</h2>
                    <p class="text-slate-600 mb-6 leading-relaxed">
                        NGN OPTIC est née de la passion pour l'optique de précision et le désir de rendre accessible l'excellence visuelle au Bénin et au-delà. Située au cœur de Porto-Novo, notre laboratoire combine savoir-faire artisanal et technologies de pointe.
                    </p>
                    <p class="text-slate-600 mb-8 leading-relaxed">
                        Nous sommes fiers d'être l'un des rares opticiens africains à offrir une livraison internationale de verres sur ordonnance, permettant à la diaspora et aux clients du monde entier de bénéficier de notre expertise.
                    </p>

                    <div class="grid grid-cols-2 gap-6">
                        <div class="flex items-start gap-3">
                            <i class="fas fa-certificate text-gold-400 text-xl mt-1"></i>
                            <div>
                                <h4 class="font-bold text-navy-900">Certifié</h4>
                                <p class="text-sm text-slate-600">Opticien diplômé d'État</p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3">
                            <i class="fas fa-shield-alt text-gold-400 text-xl mt-1"></i>
                            <div>
                                <h4 class="font-bold text-navy-900">Garantie</h4>
                                <p class="text-sm text-slate-600">2 ans sur tous les verres</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-24 bg-navy-900 relative overflow-hidden">
        <div class="absolute inset-0 hero-pattern opacity-10"></div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid md:grid-cols-2 gap-16">
                <div class="scroll-reveal">
                    <h2 class="font-serif text-4xl md:text-5xl font-bold text-white mb-6">Contactez-Nous</h2>
                    <p class="text-slate-300 mb-8 text-lg">
                        Besoin d'un rendez-vous pour un test de vue ou d'un devis pour des verres ? Notre équipe vous répond sous 24h.
                    </p>

                    <div class="space-y-6">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-gold-400/20 rounded-lg flex items-center justify-center flex-shrink-0">
                                <i class="fas fa-map-marker-alt text-gold-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-semibold mb-1">Adresse</h4>
                                <p class="text-slate-400">République du Bénin<br>Porto-Novo</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-gold-400/20 rounded-lg flex items-center justify-center flex-shrink-0">
                                <i class="fas fa-phone-alt text-gold-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-semibold mb-1">Téléphone</h4>
                                <p class="text-slate-400">
                                    <a href="tel:+2290197488477" class="hover:text-gold-400 transition-colors">+229 01 97 48 84 77</a><br>
                                    <a href="tel:+2290160868600" class="hover:text-gold-400 transition-colors">+229 01 60 86 86 00</a>
                                </p>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-gold-400/20 rounded-lg flex items-center justify-center flex-shrink-0">
                                <i class="fab fa-whatsapp text-gold-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-semibold mb-1">WhatsApp</h4>
                                <a href="https://wa.me/2290197488477" target="_blank" class="text-slate-400 hover:text-green-400 transition-colors">
                                    Discuter sur WhatsApp
                                </a>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-gold-400/20 rounded-lg flex items-center justify-center flex-shrink-0">
                                <i class="fas fa-clock text-gold-400 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-semibold mb-1">Horaires</h4>
                                <p class="text-slate-400">Lun - Sam : 8h00 - 18h30<br>Dimanche : Sur rendez-vous</p>
                            </div>
                        </div>
                    </div>

                    <div class="mt-10 flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-gold-400 hover:text-navy-900 transition-all">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-gold-400 hover:text-navy-900 transition-all">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-gold-400 hover:text-navy-900 transition-all">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>

                <div class="scroll-reveal">
                    <form class="bg-white/5 backdrop-blur-lg p-8 rounded-2xl border border-white/10" onsubmit="event.preventDefault(); alert('Message envoyé ! Nous vous contacterons sous peu.');">
                        <div class="grid md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-white text-sm font-medium mb-2">Nom</label>
                                <input type="text" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg text-white placeholder-slate-400 focus:outline-none focus:border-gold-400 transition-colors" placeholder="Votre nom">
                            </div>
                            <div>
                                <label class="block text-white text-sm font-medium mb-2">Téléphone</label>
                                <input type="tel" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg text-white placeholder-slate-400 focus:outline-none focus:border-gold-400 transition-colors" placeholder="+229 XX XX XX XX">
                            </div>
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-white text-sm font-medium mb-2">Email</label>
                            <input type="email" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg text-white placeholder-slate-400 focus:outline-none focus:border-gold-400 transition-colors" placeholder="votre@email.com">
                        </div>

                        <div class="mb-6">
                            <label class="block text-white text-sm font-medium mb-2">Service demandé</label>
                            <select class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg text-white focus:outline-none focus:border-gold-400 transition-colors">
                                <option value="" class="bg-navy-900">Choisir un service</option>
                                <option value="test" class="bg-navy-900">Test de vue</option>
                                <option value="medical" class="bg-navy-900">Verres médicaux</option>
                                <option value="solaire" class="bg-navy-900">Verres solaires</option>
                                <option value="devis" class="bg-navy-900">Demande de devis</option>
                            </select>
                        </div>

                        <div class="mb-6">
                            <label class="block text-white text-sm font-medium mb-2">Message</label>
                            <textarea rows="4" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg text-white placeholder-slate-400 focus:outline-none focus:border-gold-400 transition-colors" placeholder="Décrivez votre besoin..."></textarea>
                        </div>

                        <button type="submit" class="w-full py-4 bg-gradient-to-r from-gold-400 to-gold-600 text-navy-900 font-bold rounded-lg hover:shadow-lg hover:shadow-gold-400/30 transition-all transform hover:-translate-y-1">
                            Envoyer la demande
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-navy-950 border-t border-white/10 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-4 gap-8 mb-8">
                <div class="col-span-2">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-8 h-8 bg-gradient-to-br from-gold-400 to-gold-600 rounded-full flex items-center justify-center">
                            <i class="fas fa-eye text-white text-sm"></i>
                        </div>
                        <span class="font-serif text-xl font-bold text-white">NGN <span class="text-gold-400">OPTIC</span></span>
                    </div>
                    <p class="text-slate-400 text-sm leading-relaxed max-w-md">
                        Votre partenaire vision au Bénin. Expertise internationale, service local. Livraison mondiale de verres d'exception.
                    </p>
                </div>
                
                <div>
                    <h4 class="text-white font-semibold mb-4">Liens rapides</h4>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><a href="#services" class="hover:text-gold-400 transition-colors">Nos Services</a></li>
                        <li><a href="#produits" class="hover:text-gold-400 transition-colors">Collections</a></li>
                        <li><a href="#about" class="hover:text-gold-400 transition-colors">À Propos</a></li>
                        <li><a href="#contact" class="hover:text-gold-400 transition-colors">Contact</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-4">Légal</h4>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Mentions légales</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">Politique de confidentialité</a></li>
                        <li><a href="#" class="hover:text-gold-400 transition-colors">CGV</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
                <p class="text-slate-500 text-sm">&copy; 2024 NGN OPTIC. Tous droits réservés.</p>
                <p class="text-slate-600 text-xs">Conçu avec excellence à Porto-Novo</p>
            </div>
        </div>
    </footer>

    <!-- WhatsApp Float Button -->
    <a href="https://wa.me/2290197488477" target="_blank" class="fixed bottom-6 right-6 w-14 h-14 bg-green-500 rounded-full flex items-center justify-center shadow-lg hover:scale-110 transition-transform z-50 animate-pulse">
        <i class="fab fa-whatsapp text-white text-2xl"></i>
    </a>

    <script>
        // Navbar scroll effect
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('bg-navy-900/95', 'backdrop-blur-lg', 'shadow-lg');
                navbar.classList.remove('bg-transparent');
            } else {
                navbar.classList.remove('bg-navy-900/95', 'backdrop-blur-lg', 'shadow-lg');
                navbar.classList.add('bg-transparent');
            }
        });

        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu when clicking on a link
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Scroll reveal animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -50px 0px"
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.scroll-reveal').forEach((el) => observer.observe(el));

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>

