---
title: Connects_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 68a85d32-9bf2-2f7c-2797-85ddd593fc37
ms.openlocfilehash: d9a3283e9ac16af8997d7e9d632e067ecec7423d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538700"
---
# <a name="connects_type-complextype-visio-xml"></a><span data-ttu-id="fc8c4-102">Connects_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fc8c4-102">Connects_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fc8c4-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="fc8c4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc8c4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fc8c4-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fc8c4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fc8c4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fc8c4-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fc8c4-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fc8c4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc8c4-109">Definición</span><span class="sxs-lookup"><span data-stu-id="fc8c4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fc8c4-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fc8c4-110">Elements and attributes</span></span>

<span data-ttu-id="fc8c4-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="fc8c4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fc8c4-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc8c4-112">Child elements</span></span>

|<span data-ttu-id="fc8c4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-113">**Element**</span></span>|<span data-ttu-id="fc8c4-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-114">**Type**</span></span>|<span data-ttu-id="fc8c4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc8c4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc8c4-116">Connect</span><span class="sxs-lookup"><span data-stu-id="fc8c4-116">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc8c4-117">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="fc8c4-117">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fc8c4-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc8c4-118">Attributes</span></span>

<span data-ttu-id="fc8c4-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fc8c4-119">None.</span></span>
  

