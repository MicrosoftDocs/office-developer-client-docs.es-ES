---
title: StyleSheets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: 1992f0e31ae972320f80f99d94164fbd1dbc6d45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395745"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="fd777-102">StyleSheets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="fd777-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fd777-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="fd777-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd777-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fd777-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fd777-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fd777-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fd777-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fd777-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fd777-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="fd777-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fd777-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fd777-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fd777-109">Definición</span><span class="sxs-lookup"><span data-stu-id="fd777-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fd777-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fd777-110">Elements and attributes</span></span>

<span data-ttu-id="fd777-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="fd777-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fd777-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fd777-112">Child elements</span></span>

|<span data-ttu-id="fd777-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd777-113">**Element**</span></span>|<span data-ttu-id="fd777-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd777-114">**Type**</span></span>|<span data-ttu-id="fd777-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd777-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fd777-116">Hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="fd777-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fd777-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="fd777-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fd777-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd777-118">Attributes</span></span>

<span data-ttu-id="fd777-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fd777-119">None.</span></span>
  

