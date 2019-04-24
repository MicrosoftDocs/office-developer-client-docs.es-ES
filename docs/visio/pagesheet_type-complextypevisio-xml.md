---
title: PageSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334653"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="ead25-102">PageSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ead25-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ead25-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ead25-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ead25-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ead25-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ead25-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ead25-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ead25-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ead25-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ead25-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ead25-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ead25-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="ead25-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ead25-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ead25-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ead25-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ead25-110">Elements and attributes</span></span>

<span data-ttu-id="ead25-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ead25-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ead25-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ead25-112">Child elements</span></span>

<span data-ttu-id="ead25-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ead25-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ead25-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ead25-114">Attributes</span></span>

|<span data-ttu-id="ead25-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ead25-115">**Attribute**</span></span>|<span data-ttu-id="ead25-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ead25-116">**Type**</span></span>|<span data-ttu-id="ead25-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ead25-117">**Required**</span></span>|<span data-ttu-id="ead25-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ead25-118">**Description**</span></span>|<span data-ttu-id="ead25-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ead25-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ead25-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ead25-120">UniqueID</span></span>  <br/> |<span data-ttu-id="ead25-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ead25-121">xsd:string</span></span>  <br/> |<span data-ttu-id="ead25-122">opcional</span><span class="sxs-lookup"><span data-stu-id="ead25-122">optional</span></span>  <br/> ||<span data-ttu-id="ead25-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ead25-123">Values of the xsd:string type.</span></span>  <br/> |
   

