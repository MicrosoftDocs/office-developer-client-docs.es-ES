---
title: StyleSheets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2603bc5-86bd-df29-43c2-25a39419ad1e
ms.openlocfilehash: a48dc8d4c8327cffc53469a8c6d8a81d021a4500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823340"
---
# <a name="stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="690da-102">StyleSheets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="690da-102">StyleSheets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="690da-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="690da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="690da-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="690da-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="690da-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="690da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="690da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="690da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="690da-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="690da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="690da-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="690da-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="690da-109">Definición</span><span class="sxs-lookup"><span data-stu-id="690da-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="690da-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="690da-110">Elements and attributes</span></span>

<span data-ttu-id="690da-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="690da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="690da-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="690da-112">Child elements</span></span>

|<span data-ttu-id="690da-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="690da-113">**Element**</span></span>|<span data-ttu-id="690da-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="690da-114">**Type**</span></span>|<span data-ttu-id="690da-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="690da-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="690da-116">Hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="690da-116">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="690da-117">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="690da-117">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="690da-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="690da-118">Attributes</span></span>

<span data-ttu-id="690da-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="690da-119">None.</span></span>
  

