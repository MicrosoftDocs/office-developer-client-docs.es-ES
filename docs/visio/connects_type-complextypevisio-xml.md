---
title: Connects_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: ed5046656554fdd64251601c12e6817d586cd689
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399882"
---
# <a name="connectstype-complextype-visio-xml"></a><span data-ttu-id="91826-102">Connects_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="91826-102">Connects_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="91826-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="91826-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91826-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="91826-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="91826-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="91826-105">**Schema file**</span></span> <br/> |<span data-ttu-id="91826-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="91826-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="91826-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="91826-107">**Extension base**</span></span> <br/> |<span data-ttu-id="91826-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="91826-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91826-109">Definición</span><span class="sxs-lookup"><span data-stu-id="91826-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="91826-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="91826-110">Elements and attributes</span></span>

<span data-ttu-id="91826-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="91826-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="91826-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91826-112">Child elements</span></span>

|<span data-ttu-id="91826-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="91826-113">**Element**</span></span>|<span data-ttu-id="91826-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="91826-114">**Type**</span></span>|<span data-ttu-id="91826-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91826-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91826-116">Connect</span><span class="sxs-lookup"><span data-stu-id="91826-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91826-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="91826-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="91826-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="91826-118">Attributes</span></span>

<span data-ttu-id="91826-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91826-119">None.</span></span>
  

