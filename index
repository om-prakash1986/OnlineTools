@model OnlineTools.Models.ImageResizerModel

@{
    ViewBag.Title = "Free Online Image Resizer - Resize Images Easily";
    ViewBag.Description = "Free online image resizer tool. Easily resize, compress and convert your images while maintaining quality. Support for JPG, PNG, and GIF formats.";
}

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online image resizer tool. Easily resize, compress and convert your images while maintaining quality. Support for JPG, PNG, and GIF formats.">
    <meta name="keywords" content="image resizer, resize image online, free image resizer, photo resizer, picture resize tool, compress image">
    <meta name="author" content="OnlineTools">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="@ViewBag.Title">
    <meta property="og:description" content="Free online image resizer tool. Easily resize, compress and convert your images while maintaining quality.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="@Request.Url.AbsoluteUri">
    <meta name="twitter:card" content="summary">
    <meta name="twitter:title" content="@ViewBag.Title">
    <meta name="twitter:description" content="Free online image resizer tool. Easily resize, compress and convert your images.">
    <link rel="canonical" href="@Request.Url.AbsoluteUri" />
    
    <title>@ViewBag.Title</title>
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f2f5;
            color: #1a1a1a;
        }
        
        .container {
            max-width: 1200px;
        }
        
        .card {
            border: none;
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .card-body {
            padding: 2rem;
        }
        
        .btn {
            padding: 0.5rem 1.5rem;
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .btn-lg {
            padding: 0.75rem 2rem;
        }
        
        .btn-primary {
            background-color: #0d6efd;
            border-color: #0d6efd;
        }
        
        .btn-primary:hover {
            background-color: #0b5ed7;
            border-color: #0a58ca;
            transform: translateY(-2px);
        }
        
        .btn-success {
            background-color: #198754;
            border-color: #198754;
        }
        
        .btn-success:hover {
            background-color: #157347;
            border-color: #146c43;
            transform: translateY(-2px);
        }
        
        .form-control {
            border-radius: 8px;
            border: 2px solid #dee2e6;
            padding: 0.75rem 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: #0d6efd;
            box-shadow: 0 0 0 0.25rem rgba(13, 110, 253, 0.25);
        }
        
        .form-floating > label {
            padding: 0.75rem 1rem;
            color: #6c757d;
        }
        
        .border-dashed {
            border-style: dashed !important;
        }
        
        .upload-area {
            background-color: #f8f9fa;
            border: 2px dashed #dee2e6;
            transition: all 0.3s ease;
        }
        
        .upload-area:hover {
            border-color: #0d6efd;
            background-color: #e9ecef;
            cursor: pointer;
        }
        
        .badge {
            padding: 0.5em 1em;
            border-radius: 6px;
            font-weight: 500;
        }
        
        .shadow-lg {
            box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.175) !important;
        }
        
        .footer {
            padding: 1rem 0;
            width: 100%;
            background-color: transparent;
        }
        
        .visitor-count .badge {
            font-size: 0.9rem;
            padding: 0.5rem 1rem;
            background-color: #6c757d;
            transition: all 0.3s ease;
            cursor: default;
        }
        
        .visitor-count .badge:hover {
            background-color: #5a6268;
            transform: translateY(-2px);
        }
        
        .visitor-count .badge i {
            color: #fff;
        }
        
        .ad-container {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 1rem;
            margin: 1rem 0;
            min-height: 100px;
        }
        
        .ad-container:empty {
            display: none;
        }
        
        @media (max-width: 768px) {
            .display-4 {
                font-size: 2.5rem;
            }
            
            .lead {
                font-size: 1.1rem;
            }
            
            .ad-container {
                padding: 0.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container py-5">
        <!-- AdSense Ad Unit - Top -->
        <div class="ad-container text-center my-3">
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="YOUR-ADSENSE-CLIENT-ID"
                 data-ad-slot="YOUR-AD-SLOT-ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="text-center mb-5">
                    <h1 class="display-4 text-primary">Free Online Image Resizer</h1>
                    <p class="lead text-muted">Resize your images quickly and easily while maintaining quality</p>
                    <div class="features mt-4">
                        <span class="badge bg-primary me-2 mb-2">✓ Free to Use</span>
                        <span class="badge bg-primary me-2 mb-2">✓ No Registration</span>
                        <span class="badge bg-primary me-2 mb-2">✓ High Quality</span>
                        <span class="badge bg-primary me-2 mb-2">✓ Multiple Formats</span>
                    </div>
                </div>

                <div class="card shadow-lg">
                    <div class="card-body p-4">
                        @using (Html.BeginForm("Resize", "ImageResizer", FormMethod.Post, new { enctype = "multipart/form-data", @class = "needs-validation" }))
                        {
                            @Html.ValidationSummary(true, "", new { @class = "alert alert-danger" })
                            
                            <div class="upload-area mb-4 text-center p-4 border-2 border-dashed rounded-3" id="dropZone">
                                <i class="fas fa-cloud-upload-alt fa-3x text-primary mb-3"></i>
                                <div class="mb-3">
                                    <label class="form-label fw-bold">Upload Image</label>
                                    @Html.TextBoxFor(m => m.ImageFile, new { type = "file", accept = "image/*", @class = "form-control d-none", id = "imageInput" })
                                    <div class="mt-2">
                                        <button type="button" class="btn btn-outline-primary btn-lg" onclick="document.getElementById('imageInput').click()">
                                            <i class="fas fa-image me-2"></i>Choose Image
                                        </button>
                                    </div>
                                </div>
                                <p class="text-muted small">Supported formats: JPEG, PNG, GIF</p>
                                @Html.ValidationMessageFor(m => m.ImageFile, "", new { @class = "text-danger" })
                                
                                <div id="imagePreview" class="mt-3 d-none">
                                    <img src="" alt="Preview" class="img-fluid rounded shadow-sm" style="max-height: 200px"/>
                                    <div class="mt-2">
                                        <span class="badge bg-info" id="originalDimensions"></span>
                                    </div>
                                </div>
                            </div>

                            <div class="row g-3 mb-4">
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        @Html.TextBoxFor(m => m.Width, new { @class = "form-control", type = "number", min = "1", max = "10000", placeholder = "Width" })
                                        <label>Width (px)</label>
                                        @Html.ValidationMessageFor(m => m.Width, "", new { @class = "text-danger small" })
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        @Html.TextBoxFor(m => m.Height, new { @class = "form-control", type = "number", min = "1", max = "10000", placeholder = "Height" })
                                        <label>Height (px)</label>
                                        @Html.ValidationMessageFor(m => m.Height, "", new { @class = "text-danger small" })
                                    </div>
                                </div>
                            </div>

                            <div class="form-check form-switch mb-4">
                                @Html.CheckBoxFor(m => m.MaintainAspectRatio, new { @class = "form-check-input", role = "switch" })
                                <label class="form-check-label">Maintain Aspect Ratio</label>
                            </div>

                            <div class="d-grid">
                                <button type="submit" class="btn btn-primary btn-lg">
                                    <i class="fas fa-crop-alt me-2"></i>Resize Image
                                </button>
                            </div>
                        }

                        @if (!string.IsNullOrEmpty(Model.ResizedImagePath))
                        {
                            <div class="result-section mt-5">
                                <h4 class="text-center mb-4">Resized Image</h4>
                                <div class="text-center">
                                    <div class="position-relative d-inline-block">
                                        <img src="@Model.ResizedImagePath" class="img-fluid rounded shadow" alt="Resized Image" />
                                        <div class="position-absolute bottom-0 start-50 translate-middle-x mb-3">
                                            <a href="@Model.ResizedImagePath" class="btn btn-success btn-lg" download>
                                                <i class="fas fa-download me-2"></i>Download
                                            </a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        }
                    </div>
                </div>

                <!-- SEO Content Section -->
                <div class="mt-5">
                    <h2 class="h4 mb-4">Why Use Our Free Image Resizer?</h2>
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="feature-card p-3 bg-light rounded">
                                <h3 class="h5 mb-3">✨ Easy to Use</h3>
                                <p class="small text-muted">No technical skills required. Simply upload your image, set dimensions, and download the resized version.</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="feature-card p-3 bg-light rounded">
                                <h3 class="h5 mb-3">🔒 Secure & Private</h3>
                                <p class="small text-muted">Your images are processed securely in your browser and are never stored on our servers.</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="feature-card p-3 bg-light rounded">
                                <h3 class="h5 mb-3">🎨 Quality Maintained</h3>
                                <p class="small text-muted">Advanced algorithms ensure your resized images maintain the best possible quality.</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="feature-card p-3 bg-light rounded">
                                <h3 class="h5 mb-3">📱 Mobile Friendly</h3>
                                <p class="small text-muted">Resize images on any device - works perfectly on desktop, tablet, and mobile.</p>
                            </div>
                        </div>
                    </div>

                    <div class="mt-5">
                        <h2 class="h4 mb-4">How to Resize Your Images</h2>
                        <ol class="list-group list-group-numbered">
                            <li class="list-group-item">Upload your image (JPG, PNG, or GIF format)</li>
                            <li class="list-group-item">Enter your desired width and height in pixels</li>
                            <li class="list-group-item">Choose whether to maintain the aspect ratio</li>
                            <li class="list-group-item">Click "Resize Image" and download your resized image</li>
                        </ol>
                    </div>

                    <div class="mt-5">
                        <h2 class="h4 mb-4">Supported Image Formats</h2>
                        <div class="row g-3">
                            <div class="col-md-4">
                                <div class="format-card p-3 bg-light rounded text-center">
                                    <h3 class="h5">JPEG/JPG</h3>
                                    <p class="small text-muted mb-0">Best for photographs</p>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="format-card p-3 bg-light rounded text-center">
                                    <h3 class="h5">PNG</h3>
                                    <p class="small text-muted mb-0">Perfect for graphics</p>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="format-card p-3 bg-light rounded text-center">
                                    <h3 class="h5">GIF</h3>
                                    <p class="small text-muted mb-0">Ideal for animations</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- AdSense Ad Unit - Bottom -->
        <div class="ad-container text-center my-3">
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="YOUR-ADSENSE-CLIENT-ID"
                 data-ad-slot="YOUR-AD-SLOT-ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>

        <footer class="footer mt-4">
            <div class="d-flex justify-content-between align-items-center">
                <p class="mb-0">&copy; @DateTime.Now.Year - Free Online Image Resizer Tool</p>
                @if (ViewBag.VisitorCount != null)
                {
                    <div class="visitor-count">
                        <span class="badge bg-secondary">
                            <i class="fas fa-users me-2"></i>Total Visitors: @ViewBag.VisitorCount
                        </span>
                    </div>
                }
            </div>
        </footer>
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-validate/1.19.3/jquery.validate.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-validation-unobtrusive/3.2.12/jquery.validate.unobtrusive.min.js"></script>
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=YOUR-ADSENSE-CLIENT-ID" crossorigin="anonymous"></script>

    <script>
        $(document).ready(function () {
            const dropZone = $('#dropZone');
            const imageInput = $('#imageInput');
            const imagePreview = $('#imagePreview');
            const originalDimensions = $('#originalDimensions');
            
            // Handle drag and drop
            dropZone.on('dragover', function(e) {
                e.preventDefault();
                $(this).addClass('bg-light');
            });
            
            dropZone.on('dragleave', function(e) {
                e.preventDefault();
                $(this).removeClass('bg-light');
            });
            
            dropZone.on('drop', function(e) {
                e.preventDefault();
                $(this).removeClass('bg-light');
                const files = e.originalEvent.dataTransfer.files;
                if (files.length > 0) {
                    imageInput[0].files = files;
                    handleImageSelect(files[0]);
                }
            });
            
            // Handle click upload
            dropZone.on('click', function() {
                imageInput.click();
            });
            
            // Preview image and set dimensions
            imageInput.change(function() {
                if (this.files && this.files[0]) {
                    handleImageSelect(this.files[0]);
                }
            });
            
            function handleImageSelect(file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = new Image();
                    img.onload = function() {
                        $('#Width').val(this.width);
                        $('#Height').val(this.height);
                        originalDimensions.text(`Original: ${this.width} × ${this.height}px`);
                    }
                    img.src = e.target.result;
                    imagePreview.find('img').attr('src', e.target.result);
                    imagePreview.removeClass('d-none');
                }
                reader.readAsDataURL(file);
            }
            
            // Handle aspect ratio
            let aspectRatio = 1;
            $('#MaintainAspectRatio').change(function() {
                if ($(this).is(':checked')) {
                    aspectRatio = $('#Width').val() / $('#Height').val();
                }
            });
            
            $('#Width').change(function() {
                if ($('#MaintainAspectRatio').is(':checked')) {
                    $('#Height').val(Math.round($(this).val() / aspectRatio));
                }
            });
            
            $('#Height').change(function() {
                if ($('#MaintainAspectRatio').is(':checked')) {
                    $('#Width').val(Math.round($(this).val() * aspectRatio));
                }
            });
        });
    </script>

    <!-- Structured Data for SEO -->
    <script type="application/ld+json">
    {
        "@@context": "http://schema.org",
        "@@type": "WebApplication",
        "name": "Free Online Image Resizer",
        "url": "@Request.Url.AbsoluteUri",
        "description": "Free online tool to resize, compress and convert images while maintaining quality. Support for JPG, PNG, and GIF formats.",
        "applicationCategory": "Image Processing Tool",
        "operatingSystem": "All",
        "offers": {
            "@@type": "Offer",
            "price": "0",
            "priceCurrency": "USD"
        },
        "featureList": [
            "Resize images online",
            "Maintain aspect ratio",
            "Support multiple formats",
            "Free to use",
            "No registration required"
        ]
    }
    </script>
</body>
</html> 
