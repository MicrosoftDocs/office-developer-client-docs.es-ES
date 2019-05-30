---
title: ComplexType ActionTagRow_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 7d2822cb0df0b18e7f19e380fc3e1ba9e4f10c69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541376"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="cca21-102">ComplexType ActionTagRow_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="cca21-102">ActionTagRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cca21-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cca21-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cca21-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cca21-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cca21-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cca21-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cca21-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cca21-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cca21-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cca21-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cca21-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="cca21-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cca21-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cca21-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="cca21-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cca21-110">Elements and attributes</span></span>

<span data-ttu-id="cca21-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cca21-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cca21-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cca21-112">Child elements</span></span>

|<span data-ttu-id="cca21-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cca21-113">**Element**</span></span>|<span data-ttu-id="cca21-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cca21-114">**Type**</span></span>|<span data-ttu-id="cca21-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cca21-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cca21-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cca21-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="cca21-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cca21-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cca21-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="cca21-118">Attributes</span></span>

<span data-ttu-id="cca21-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cca21-119">None.</span></span>
  

