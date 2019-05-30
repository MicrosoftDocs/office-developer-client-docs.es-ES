---
title: ComplexType FieldRow_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3474d268-4435-cb4d-9c66-a30924635e20
ms.openlocfilehash: f6102c89cc0e484b1a07fb11bf26285df8954a5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542362"
---
# <a name="fieldrowtype-complextype-visio-xml"></a><span data-ttu-id="e1e57-102">ComplexType FieldRow_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="e1e57-102">FieldRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e1e57-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e1e57-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1e57-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e1e57-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e1e57-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e1e57-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e1e57-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e1e57-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e1e57-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e1e57-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e1e57-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e1e57-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1e57-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e1e57-109">Definition</span></span>

```XML
          <xs:complexType name="FieldRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e1e57-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e1e57-110">Elements and attributes</span></span>

<span data-ttu-id="e1e57-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e1e57-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e1e57-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1e57-112">Child elements</span></span>

|<span data-ttu-id="e1e57-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e1e57-113">**Element**</span></span>|<span data-ttu-id="e1e57-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e1e57-114">**Type**</span></span>|<span data-ttu-id="e1e57-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1e57-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1e57-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e1e57-116">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e1e57-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e1e57-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e1e57-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1e57-118">Attributes</span></span>

<span data-ttu-id="e1e57-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1e57-119">None.</span></span>
  

