---
title: RowDef_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64897258-dd7e-a730-d4f5-d9c217308491
ms.openlocfilehash: e097e740b543661e5c49a81d75c047c8749ce1d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564258"
---
# <a name="rowdeftype-complextype-visio-xml"></a><span data-ttu-id="beacd-102">RowDef_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="beacd-102">RowDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="beacd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="beacd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beacd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="beacd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="beacd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="beacd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="beacd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="beacd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="beacd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="beacd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="beacd-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="beacd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="beacd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="beacd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="beacd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="beacd-110">Elements and attributes</span></span>

<span data-ttu-id="beacd-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="beacd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="beacd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="beacd-112">Child elements</span></span>

|<span data-ttu-id="beacd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="beacd-113">**Element**</span></span>|<span data-ttu-id="beacd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="beacd-114">**Type**</span></span>|<span data-ttu-id="beacd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="beacd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="beacd-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="beacd-116">CellDef</span></span> <br/> |[<span data-ttu-id="beacd-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="beacd-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="beacd-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="beacd-118">Attributes</span></span>

<span data-ttu-id="beacd-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="beacd-119">None.</span></span>
  

