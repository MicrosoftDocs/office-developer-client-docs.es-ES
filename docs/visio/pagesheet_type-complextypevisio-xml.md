---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540591"
---
# <a name="pagesheet_type-complextype-visio-xml"></a><span data-ttu-id="38e42-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="38e42-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="38e42-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="38e42-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38e42-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38e42-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="38e42-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="38e42-105">**Schema file**</span></span> <br/> |<span data-ttu-id="38e42-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="38e42-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="38e42-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="38e42-107">**Extension base**</span></span> <br/> |<span data-ttu-id="38e42-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="38e42-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38e42-109">Definición</span><span class="sxs-lookup"><span data-stu-id="38e42-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="38e42-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="38e42-110">Elements and attributes</span></span>

<span data-ttu-id="38e42-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="38e42-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="38e42-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38e42-112">Child elements</span></span>

<span data-ttu-id="38e42-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38e42-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38e42-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="38e42-114">Attributes</span></span>

|<span data-ttu-id="38e42-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="38e42-115">**Attribute**</span></span>|<span data-ttu-id="38e42-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38e42-116">**Type**</span></span>|<span data-ttu-id="38e42-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="38e42-117">**Required**</span></span>|<span data-ttu-id="38e42-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38e42-118">**Description**</span></span>|<span data-ttu-id="38e42-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="38e42-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38e42-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="38e42-120">UniqueID</span></span>  <br/> |<span data-ttu-id="38e42-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38e42-121">xsd:string</span></span>  <br/> |<span data-ttu-id="38e42-122">opcional</span><span class="sxs-lookup"><span data-stu-id="38e42-122">optional</span></span>  <br/> ||<span data-ttu-id="38e42-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="38e42-123">Values of the xsd:string type.</span></span>  <br/> |
   

