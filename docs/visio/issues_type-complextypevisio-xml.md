---
title: Issues_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822386"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="c3a94-102">Issues_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="c3a94-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c3a94-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c3a94-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3a94-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3a94-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3a94-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c3a94-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3a94-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c3a94-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3a94-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c3a94-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3a94-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c3a94-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3a94-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c3a94-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3a94-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c3a94-110">Elements and attributes</span></span>

<span data-ttu-id="c3a94-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="c3a94-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3a94-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3a94-112">Child elements</span></span>

|<span data-ttu-id="c3a94-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3a94-113">**Element**</span></span>|<span data-ttu-id="c3a94-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3a94-114">**Type**</span></span>|<span data-ttu-id="c3a94-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3a94-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3a94-116">Problema</span><span class="sxs-lookup"><span data-stu-id="c3a94-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3a94-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="c3a94-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c3a94-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3a94-118">Attributes</span></span>

<span data-ttu-id="c3a94-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3a94-119">None.</span></span>
  

