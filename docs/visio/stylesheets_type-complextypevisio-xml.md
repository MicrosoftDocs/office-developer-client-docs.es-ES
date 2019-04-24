---
title: StyleSheets_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346784"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="9d2a2-102">StyleSheets_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9d2a2-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9d2a2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9d2a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d2a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9d2a2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9d2a2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9d2a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9d2a2-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9d2a2-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d2a2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d2a2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9d2a2-109">Definition</span></span>

```XML
          <xs:complexType name="StyleSheets_Type">
          
          <xs:sequence>
    <xs:element name="StyleSheet"  type="StyleSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d2a2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9d2a2-110">Elements and attributes</span></span>

<span data-ttu-id="9d2a2-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9d2a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9d2a2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d2a2-112">Child elements</span></span>

|<span data-ttu-id="9d2a2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-113">**Element**</span></span>|<span data-ttu-id="9d2a2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-114">**Type**</span></span>|<span data-ttu-id="9d2a2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d2a2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d2a2-116">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="9d2a2-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d2a2-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9d2a2-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9d2a2-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d2a2-118">Attributes</span></span>

<span data-ttu-id="9d2a2-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9d2a2-119">None.</span></span>
  

