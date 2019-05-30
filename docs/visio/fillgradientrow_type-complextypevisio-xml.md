---
title: ComplexType FillGradientRow_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40c88316-4710-b5b4-7be4-e3047474d519
ms.openlocfilehash: c16eacef6afee8e90b5fb6a0e6844fcbd9735c0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539631"
---
# <a name="fillgradientrowtype-complextype-visio-xml"></a><span data-ttu-id="277b5-102">ComplexType FillGradientRow_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="277b5-102">FillGradientRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="277b5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="277b5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="277b5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="277b5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="277b5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="277b5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="277b5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="277b5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="277b5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="277b5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="277b5-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="277b5-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="277b5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="277b5-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="277b5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="277b5-110">Elements and attributes</span></span>

<span data-ttu-id="277b5-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="277b5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="277b5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="277b5-112">Child elements</span></span>

|<span data-ttu-id="277b5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="277b5-113">**Element**</span></span>|<span data-ttu-id="277b5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="277b5-114">**Type**</span></span>|<span data-ttu-id="277b5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="277b5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="277b5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="277b5-116">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="277b5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="277b5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="277b5-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="277b5-118">Attributes</span></span>

<span data-ttu-id="277b5-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="277b5-119">None.</span></span>
  

