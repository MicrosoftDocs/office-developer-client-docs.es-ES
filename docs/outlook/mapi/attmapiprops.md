---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318126"
---
# <a name="attmapiprops"></a><span data-ttu-id="e9445-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="e9445-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="e9445-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9445-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9445-105">El atributo **attMAPIProps** es especial en que se puede usar para codificar cualquier propiedad MAPI que no tenga un homólogo en el conjunto de atributos definidos de TNEF existentes.</span><span class="sxs-lookup"><span data-stu-id="e9445-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="e9445-106">Los datos de atributo son un conjunto contado de propiedades MAPI que se establecen de extremo a extremo.</span><span class="sxs-lookup"><span data-stu-id="e9445-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="e9445-107">El formato de esta codificación, que permite cualquier conjunto de propiedades MAPI, es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="e9445-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="e9445-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="e9445-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="e9445-109">propiedad-Count _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="e9445-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="e9445-110">Debe haber tantos elementos _Property_Value_ como indique Property-Count Value.</span><span class="sxs-lookup"><span data-stu-id="e9445-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="e9445-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="e9445-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="e9445-112">propiedad-Tag _Property_property-tag _Proptag_Name_</span><span class="sxs-lookup"><span data-stu-id="e9445-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="e9445-113">La etiqueta de propiedad es simplemente el valor asociado al identificador de la propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9445-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="e9445-114">_Inspector_</span><span class="sxs-lookup"><span data-stu-id="e9445-114">_Property:_</span></span>
  
>  <span data-ttu-id="e9445-115">__ Valor de valor _,..._ de valor de recuento</span><span class="sxs-lookup"><span data-stu-id="e9445-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="e9445-116">_Valor:_</span><span class="sxs-lookup"><span data-stu-id="e9445-116">_Value:_</span></span>
  
> <span data-ttu-id="e9445-117">valor de datos de valor-valor de tamaño-valor de relleno de datos-valor de tamaño-valor de IID-relleno de datos</span><span class="sxs-lookup"><span data-stu-id="e9445-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="e9445-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="e9445-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="e9445-119">Name-GUID nombre-tipo nombre-ID nombre-identificador GUID nombre de la clase-cadena-longitud nombre-cadena-relleno</span><span class="sxs-lookup"><span data-stu-id="e9445-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="e9445-120">La encapsulación de cada propiedad varía en función del identificador de propiedad y del tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9445-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="e9445-121">Las etiquetas de propiedad, los identificadores y los tipos se definen en los archivos de encabezado Mapitags. h y Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="e9445-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="e9445-122">Si la propiedad es una propiedad con nombre, la etiqueta de propiedad va seguida inmediatamente por el nombre de la propiedad MAPI, formado por un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="e9445-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="e9445-123">Las propiedades y propiedades multivalor con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o PT Object, se tratan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e9445-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="e9445-124">En primer lugar, se coloca en la secuencia TNEF el número de valores, codificado como 32-bit unsigned Long, seguido de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="e9445-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="e9445-125">Los datos de valor de cada propiedad se codifican como su tamaño en bytes seguidos de los propios datos de valor.</span><span class="sxs-lookup"><span data-stu-id="e9445-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="e9445-126">Los datos de valor se rellenan a un límite de 4 bytes, aunque la cantidad de relleno no se incluye en el tamaño del valor.</span><span class="sxs-lookup"><span data-stu-id="e9445-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="e9445-127">Si la propiedad es del tipo PT Object, el tamaño del valor va seguido del identificador de interfaz del objeto.</span><span class="sxs-lookup"><span data-stu-id="e9445-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="e9445-128">La implementación actual de TNEF solo admite los identificadores de interfaz IID_IMessage, IID_IStorage y IID_Istream.</span><span class="sxs-lookup"><span data-stu-id="e9445-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="e9445-129">El tamaño del identificador de interfaz se incluye en el valor-size.</span><span class="sxs-lookup"><span data-stu-id="e9445-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="e9445-130">Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT Object y un identificador de interfaz de IID_Imessage), los datos del valor se codifican como una secuencia TNEF incrustada.</span><span class="sxs-lookup"><span data-stu-id="e9445-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="e9445-131">La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF para la secuencia original y procesando la secuencia en línea.</span><span class="sxs-lookup"><span data-stu-id="e9445-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

