---
title: RowDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: 79a01d9fe5edf1de933f05683eca3bfd6e95e4b3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538140"
---
# <a name="rowdef_type-complextype-visio-xml"></a><span data-ttu-id="b254c-102">RowDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b254c-102">RowDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b254c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b254c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b254c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b254c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b254c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b254c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b254c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b254c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b254c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b254c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b254c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b254c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b254c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b254c-109">Definition</span></span>

```XML
          <xs:complexType name="RowDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b254c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b254c-110">Elements and attributes</span></span>

<span data-ttu-id="b254c-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b254c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b254c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b254c-112">Child elements</span></span>

|<span data-ttu-id="b254c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b254c-113">**Element**</span></span>|<span data-ttu-id="b254c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b254c-114">**Type**</span></span>|<span data-ttu-id="b254c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b254c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b254c-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="b254c-116">CellDef</span></span> <br/> |[<span data-ttu-id="b254c-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="b254c-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b254c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b254c-118">Attributes</span></span>

<span data-ttu-id="b254c-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b254c-119">None.</span></span>
  

