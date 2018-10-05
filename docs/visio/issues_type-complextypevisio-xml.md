---
title: Issues_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 42482db0c4542398381bc02ec5b21a8b80fac62f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397236"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="1ed8f-102">Issues_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1ed8f-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ed8f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1ed8f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ed8f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ed8f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ed8f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ed8f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ed8f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ed8f-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1ed8f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ed8f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1ed8f-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ed8f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1ed8f-110">Elements and attributes</span></span>

<span data-ttu-id="1ed8f-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1ed8f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ed8f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ed8f-112">Child elements</span></span>

|<span data-ttu-id="1ed8f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-113">**Element**</span></span>|<span data-ttu-id="1ed8f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-114">**Type**</span></span>|<span data-ttu-id="1ed8f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ed8f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ed8f-116">Problema</span><span class="sxs-lookup"><span data-stu-id="1ed8f-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ed8f-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="1ed8f-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1ed8f-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ed8f-118">Attributes</span></span>

<span data-ttu-id="1ed8f-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ed8f-119">None.</span></span>
  

