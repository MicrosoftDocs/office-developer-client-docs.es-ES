---
title: PageSheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822725"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="cbf38-102">PageSheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="cbf38-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cbf38-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cbf38-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbf38-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cbf38-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cbf38-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cbf38-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cbf38-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cbf38-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cbf38-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="cbf38-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cbf38-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="cbf38-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cbf38-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cbf38-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cbf38-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cbf38-110">Elements and attributes</span></span>

<span data-ttu-id="cbf38-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="cbf38-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cbf38-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cbf38-112">Child elements</span></span>

<span data-ttu-id="cbf38-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cbf38-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbf38-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cbf38-114">Attributes</span></span>

|<span data-ttu-id="cbf38-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cbf38-115">**Attribute**</span></span>|<span data-ttu-id="cbf38-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cbf38-116">**Type**</span></span>|<span data-ttu-id="cbf38-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cbf38-117">**Required**</span></span>|<span data-ttu-id="cbf38-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cbf38-118">**Description**</span></span>|<span data-ttu-id="cbf38-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="cbf38-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cbf38-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="cbf38-120">UniqueID</span></span>  <br/> |<span data-ttu-id="cbf38-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cbf38-121">xsd:string</span></span>  <br/> |<span data-ttu-id="cbf38-122">opcional</span><span class="sxs-lookup"><span data-stu-id="cbf38-122">optional</span></span>  <br/> ||<span data-ttu-id="cbf38-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cbf38-123">Values of the xsd:string type.</span></span>  <br/> |
   

