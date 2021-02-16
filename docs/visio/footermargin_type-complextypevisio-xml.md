---
title: FooterMargin_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f5838855a5c21b699c7a81849b9afc40790f3d01
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538644"
---
# <a name="footermargin_type-complextype-visio-xml"></a><span data-ttu-id="010c2-102">FooterMargin_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="010c2-102">FooterMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="010c2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="010c2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="010c2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="010c2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="010c2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="010c2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="010c2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="010c2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="010c2-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="010c2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="010c2-108">xsd:double</span><span class="sxs-lookup"><span data-stu-id="010c2-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="010c2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="010c2-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="010c2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="010c2-110">Elements and attributes</span></span>

<span data-ttu-id="010c2-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="010c2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="010c2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="010c2-112">Child elements</span></span>

<span data-ttu-id="010c2-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="010c2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="010c2-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="010c2-114">Attributes</span></span>

|<span data-ttu-id="010c2-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="010c2-115">**Attribute**</span></span>|<span data-ttu-id="010c2-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="010c2-116">**Type**</span></span>|<span data-ttu-id="010c2-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="010c2-117">**Required**</span></span>|<span data-ttu-id="010c2-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="010c2-118">**Description**</span></span>|<span data-ttu-id="010c2-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="010c2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="010c2-120">Unit</span><span class="sxs-lookup"><span data-stu-id="010c2-120">Unit</span></span>  <br/> |<span data-ttu-id="010c2-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="010c2-121">xsd:string</span></span>  <br/> |<span data-ttu-id="010c2-122">opcional</span><span class="sxs-lookup"><span data-stu-id="010c2-122">optional</span></span>  <br/> ||<span data-ttu-id="010c2-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="010c2-123">Values of the xsd:string type.</span></span>  <br/> |
   

