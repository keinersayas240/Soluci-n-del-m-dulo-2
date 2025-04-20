<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menú Restaurante</title>
    <style>
        /* Estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            padding: 30px;
            max-width: 800px;
            margin: 0 auto;
        }
        
        /* Título del menú */
        h1 {
            text-align: center;
            margin-bottom: 40px;
            font-size: 42px;
            color: #222;
            font-weight: 700;
            position: relative;
            padding-bottom: 15px;
        }
        
        h1::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: #c14545;
        }
        
        /* Contenedor de artículos del menú */
        .menu-container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        /* Artículo individual del menú */
        .menu-item {
            display: flex;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            background-color: white;
            position: relative;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }
        
        /* Descripción del platillo */
        .description {
            background-color: #ffffff;
            padding: 25px;
            flex-grow: 1;
            font-size: 16px;
            position: relative;
            border-left: 1px solid #eee;
        }
        
        /* Categoría del platillo */
        .category {
            width: 150px;
            min-width: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            text-align: center;
            padding: 20px;
            font-size: 20px;
            letter-spacing: 1px;
            text-transform: uppercase;
            position: relative;
            overflow: hidden;
        }
        
        /* Estilos específicos para cada categoría */
        .chicken {
            background: linear-gradient(135deg, #f1a5a5, #e27979);
            color: #4a2727;
        }
        
        .beef {
            background: linear-gradient(135deg, #d85555, #9c2b2b);
        }
        
        .sushi {
            background: linear-gradient(135deg, #f3e0a7, #d9c066);
            color: #5a4e20;
        }
        
        /* Efecto de fondo en las categorías */
        .category::before {
            content: '';
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            background: radial-gradient(circle at center, rgba(255,255,255,0.2) 0%, rgba(255,255,255,0) 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .menu-item:hover .category::before {
            opacity: 1;
        }
        
        /* Efectos adicionales para mejorar la experiencia de usuario */
        .menu-item::after {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 4px;
            height: 0;
            background-color: #c14545;
            transition: height 0.3s ease;
        }
        
        .menu-item:hover::after {
            height: 100%;
        }
        
        /* Responsive design */
        @media (max-width: 600px) {
            .menu-item {
                flex-direction: column-reverse;
            }
            
            .category {
                width: 100%;
                min-height: 60px;
            }
            
            h1 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    <h1>Our Menu</h1>
    
    <div class="menu-container">
        <div class="menu-item">
            <div class="description">
                Pechuga de pollo a la parrilla marinada con hierbas aromáticas y limón, 
                servida con puré de papas y verduras salteadas. Preparada con ingredientes 
                frescos de la más alta calidad para brindar una experiencia gastronómica única.
            </div>
            <div class="category chicken">Chicken</div>
        </div>
        
        <div class="menu-item">
            <div class="description">
                Corte de res premium cocinado al término de su preferencia, 
                acompañado de salsa de champiñones, papas fritas caseras y ensalada fresca. 
                Nuestra carne es 100% natural y proviene de ganado alimentado con pasto.
            </div>
            <div class="category beef">Beef</div>
        </div>
        
        <div class="menu-item">
            <div class="description">
                Selección de nigiri y maki preparados por nuestro chef japonés. 
                Incluye salmón fresco, atún, camarón y aguacate. Servido con 
                salsa de soya, wasabi y jengibre encurtido tradicional.
            </div>
            <div class="category sushi">Sushi</div>
        </div>
    </div>
</body>
</html>
