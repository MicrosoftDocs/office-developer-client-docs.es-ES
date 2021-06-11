---
title: Character_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 94a2aab3-6220-0cc5-ddc8-77a785821985
ms.openlocfilehash: c84a8d71fc2f080600a20625087d7c252bdcb3eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540206"
---
# <a name="character_type-complextype-visio-xml"></a><span data-ttu-id="26e07-102">Character_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="26e07-102">Character_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="26e07-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="26e07-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26e07-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26e07-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="26e07-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="26e07-105">**Schema file**</span></span> <br/> |<span data-ttu-id="26e07-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="26e07-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="26e07-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="26e07-107">**Extension base**</span></span> <br/> |<span data-ttu-id="26e07-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="26e07-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26e07-109">Definición</span><span class="sxs-lookup"><span data-stu-id="26e07-109">Definition</span></span>

```XML
          <xs:complexType name="Character_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="CharacterRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26e07-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="26e07-110">Elements and attributes</span></span>

<span data-ttu-id="26e07-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="26e07-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="26e07-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26e07-112">Child elements</span></span>

|<span data-ttu-id="26e07-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26e07-113">**Element**</span></span>|<span data-ttu-id="26e07-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26e07-114">**Type**</span></span>|<span data-ttu-id="26e07-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26e07-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26e07-116">Row</span><span class="sxs-lookup"><span data-stu-id="26e07-116">Row</span></span>](row-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="26e07-117">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="26e07-117">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="26e07-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="26e07-118">Attributes</span></span>

<span data-ttu-id="26e07-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26e07-119">None.</span></span>
  

