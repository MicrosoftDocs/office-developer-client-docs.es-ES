---
title: Connects_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: 4d2740bc0ee0934b28bbebbc10ca9c861c563be0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821854"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="673d2-102">Connects_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="673d2-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="673d2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="673d2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="673d2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="673d2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="673d2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="673d2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="673d2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="673d2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="673d2-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="673d2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="673d2-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="673d2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="673d2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="673d2-109">Definition</span></span>

```XML
          <xs:complexType name="Connects_Type">
          
          <xs:sequence>
    <xs:element name="Connect"  type="Connect_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="673d2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="673d2-110">Elements and attributes</span></span>

<span data-ttu-id="673d2-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="673d2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="673d2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="673d2-112">Child elements</span></span>

|<span data-ttu-id="673d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="673d2-113">**Element**</span></span>|<span data-ttu-id="673d2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="673d2-114">**Type**</span></span>|<span data-ttu-id="673d2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="673d2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="673d2-116">Connect</span><span class="sxs-lookup"><span data-stu-id="673d2-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="673d2-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="673d2-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="673d2-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="673d2-118">Attributes</span></span>

<span data-ttu-id="673d2-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="673d2-119">None.</span></span>
  

