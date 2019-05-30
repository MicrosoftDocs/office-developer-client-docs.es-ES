---
title: ComplexType PublishSettings_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cf14299e-8d21-0eed-bbd7-ad33d4f03533
ms.openlocfilehash: 05bf2d6ec7e0b7d05f5aa85351c266712dcee851
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538924"
---
# <a name="publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="d8317-102">ComplexType PublishSettings_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="d8317-102">PublishSettings_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d8317-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d8317-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8317-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8317-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8317-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8317-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8317-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d8317-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8317-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d8317-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8317-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d8317-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8317-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d8317-109">Definition</span></span>

```XML
          <xs:complexType name="PublishSettings_Type">
          
          <xs:sequence>
    <xs:element name="PublishedPage"  type="PublishedPage_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshableData"  type="RefreshableData_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8317-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d8317-110">Elements and attributes</span></span>

<span data-ttu-id="d8317-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d8317-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8317-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8317-112">Child elements</span></span>

|<span data-ttu-id="d8317-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8317-113">**Element**</span></span>|<span data-ttu-id="d8317-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8317-114">**Type**</span></span>|<span data-ttu-id="d8317-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8317-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8317-116">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="d8317-116">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8317-117">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="d8317-117">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d8317-118">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="d8317-118">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8317-119">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="d8317-119">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d8317-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8317-120">Attributes</span></span>

<span data-ttu-id="d8317-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8317-121">None.</span></span>
  

