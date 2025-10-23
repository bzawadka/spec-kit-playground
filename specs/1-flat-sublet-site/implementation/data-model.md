# Data Model

## Content Structure

### Apartment Images
```yaml
Living Room:
  - files: [1.jpg, 2.jpg, 3.jpg, 4.jpg, 6.png]
  - description: "Living room views"
  - order: 1

Balcony:
  - file: 5.jpg
  - description: "Balcony view"
  - order: 2

Master Bedroom:
  - files: [7.jpg, 8.jpg]
  - description: "Master bedroom views"
  - order: 3
  - related: "ensuite-bathroom"

Children Bedrooms:
  - files: [9.jpg, 10.jpg]
  - description: "Children's bedrooms"
  - order: 4

Bathrooms:
  - ensuite:
    - file: 11.jpg
    - description: "Master bedroom ensuite"
    - order: 5
  - main:
    - file: 12.jpg
    - description: "Main bathroom"
    - order: 6

Floor Plan:
  - file: plan.png
  - description: "Apartment floor plan"
  - order: 7
```

### Contact Information
```yaml
Contact:
  email: string
  phone: string
  whatsapp:
    qr_code: image/png
```

### Page Sections
```yaml
sections:
  - hero:
      title: string
      subtitle: string
      main_image: string
  
  - quick_info:
      price: string
      availability: string
      size: string
      bedrooms: number
      bathrooms: number
  
  - gallery:
      images: Image[]
      categories: string[]
  
  - features:
      amenities: string[]
      highlights: string[]
  
  - location:
      neighborhood: string
      transport: string[]
      amenities: string[]
  
  - contact:
      methods: ContactInformation
```

## File Organization
```
root/
├── index.html
├── css/
│   └── styles.css (compiled Tailwind)
└── img/
    ├── 1.jpg through 12.jpg
    └── plan.png
```