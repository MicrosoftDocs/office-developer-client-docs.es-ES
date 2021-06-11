---
title: ActionsRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32777219-850b-9526-425f-bcb017c45093
ms.openlocfilehash: 39956ec4686375a08a5d491dec388cb2ed6ba67b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540472"
---
# <a name="actionsrow_type-complextype-visio-xml"></a><span data-ttu-id="7c4bb-102">ActionsRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7c4bb-102">ActionsRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7c4bb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7c4bb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c4bb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c4bb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c4bb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7c4bb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c4bb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c4bb-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="7c4bb-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c4bb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="7c4bb-109">Definition</span></span>

```XML
          <xs:complexType name="ActionsRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c4bb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7c4bb-110">Elements and attributes</span></span>

<span data-ttu-id="7c4bb-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7c4bb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c4bb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7c4bb-112">Child elements</span></span>

|<span data-ttu-id="7c4bb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-113">**Element**</span></span>|<span data-ttu-id="7c4bb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-114">**Type**</span></span>|<span data-ttu-id="7c4bb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c4bb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c4bb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="7c4bb-116">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="7c4bb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7c4bb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7c4bb-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c4bb-118">Attributes</span></span>

<span data-ttu-id="7c4bb-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c4bb-119">None.</span></span>
  

