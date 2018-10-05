---
title: FaceNames_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 6f9cd84dffc22f4211a8445a2d493ef7d4f4a4f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387149"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="5a0f0-102">FaceNames_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5a0f0-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5a0f0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5a0f0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a0f0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5a0f0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5a0f0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5a0f0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5a0f0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5a0f0-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5a0f0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5a0f0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5a0f0-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5a0f0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5a0f0-110">Elements and attributes</span></span>

<span data-ttu-id="5a0f0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5a0f0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5a0f0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a0f0-112">Child elements</span></span>

|<span data-ttu-id="5a0f0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-113">**Element**</span></span>|<span data-ttu-id="5a0f0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-114">**Type**</span></span>|<span data-ttu-id="5a0f0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a0f0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5a0f0-116">Nombre de fuente</span><span class="sxs-lookup"><span data-stu-id="5a0f0-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5a0f0-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="5a0f0-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5a0f0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a0f0-118">Attributes</span></span>

<span data-ttu-id="5a0f0-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a0f0-119">None.</span></span>
  

