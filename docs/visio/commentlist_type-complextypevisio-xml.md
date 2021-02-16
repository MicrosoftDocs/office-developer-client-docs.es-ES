---
title: CommentList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542054"
---
# <a name="commentlist_type-complextype-visio-xml"></a><span data-ttu-id="dd8d1-102">CommentList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dd8d1-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dd8d1-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="dd8d1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd8d1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dd8d1-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dd8d1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dd8d1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dd8d1-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dd8d1-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dd8d1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dd8d1-109">Definición</span><span class="sxs-lookup"><span data-stu-id="dd8d1-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dd8d1-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="dd8d1-110">Elements and attributes</span></span>

<span data-ttu-id="dd8d1-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="dd8d1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dd8d1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd8d1-112">Child elements</span></span>

|<span data-ttu-id="dd8d1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-113">**Element**</span></span>|<span data-ttu-id="dd8d1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-114">**Type**</span></span>|<span data-ttu-id="dd8d1-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd8d1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dd8d1-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="dd8d1-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dd8d1-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="dd8d1-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dd8d1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd8d1-118">Attributes</span></span>

<span data-ttu-id="dd8d1-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd8d1-119">None.</span></span>
  

