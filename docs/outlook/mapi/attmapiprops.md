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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410458"
---
# <a name="attmapiprops"></a><span data-ttu-id="44dc7-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="44dc7-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="44dc7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44dc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44dc7-105">El **atributo attMAPIProps** es especial en que se puede usar para codificar cualquier propiedad MAPI que no tenga un equivalente en el conjunto de atributos definidos por TNEF existentes.</span><span class="sxs-lookup"><span data-stu-id="44dc7-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="44dc7-106">Los datos de atributo son un conjunto contada de propiedades MAPI colocadas de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="44dc7-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="44dc7-107">El formato de esta codificación, que permite cualquier conjunto de propiedades MAPI, es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="44dc7-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="44dc7-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="44dc7-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="44dc7-109">cuenta de  _propiedades Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="44dc7-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="44dc7-110">Debe haber tantos elementos  _Property_Value_ como indique el valor de recuento de propiedades.</span><span class="sxs-lookup"><span data-stu-id="44dc7-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="44dc7-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="44dc7-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="44dc7-112">property-tag _Property_property-tag  _Proptag_Name Property_</span><span class="sxs-lookup"><span data-stu-id="44dc7-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="44dc7-113">La etiqueta de propiedad es simplemente el valor asociado con el identificador de propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="44dc7-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="44dc7-114">_Propiedad:_</span><span class="sxs-lookup"><span data-stu-id="44dc7-114">_Property:_</span></span>
  
>  <span data-ttu-id="44dc7-115">_Valor_ de recuento de  _valores,..._</span><span class="sxs-lookup"><span data-stu-id="44dc7-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="44dc7-116">_Valor:_</span><span class="sxs-lookup"><span data-stu-id="44dc7-116">_Value:_</span></span>
  
> <span data-ttu-id="44dc7-117">value-data value-size value-data padding value-size value-IID value-data padding</span><span class="sxs-lookup"><span data-stu-id="44dc7-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="44dc7-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="44dc7-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="44dc7-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="44dc7-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="44dc7-120">La encapsulación de cada propiedad varía según el identificador de propiedad y el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="44dc7-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="44dc7-121">Las etiquetas de propiedad, los identificadores y los tipos se definen en los archivos de encabezado Mapitags.h y Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="44dc7-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="44dc7-122">Si la propiedad es una propiedad con nombre, la etiqueta de propiedad va seguida inmediatamente del nombre de la propiedad MAPI, que consta de un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="44dc7-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="44dc7-123">Las propiedades y propiedades multivalor con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o PT_OBJECT, se tratan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="44dc7-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="44dc7-124">En primer lugar, el número de valores, codificado como un long sin signo de 32 bits, se coloca en la secuencia TNEF, seguido de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="44dc7-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="44dc7-125">Los datos de valor de cada propiedad se codifican como su tamaño en bytes seguidos de los propios datos de valor.</span><span class="sxs-lookup"><span data-stu-id="44dc7-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="44dc7-126">Los datos de valor se agregan a un límite de 4 bytes, aunque la cantidad de espaciado interno no se incluye en el tamaño del valor.</span><span class="sxs-lookup"><span data-stu-id="44dc7-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="44dc7-127">Si la propiedad es de tipo PT_OBJECT, el valor-tamaño va seguido del identificador de interfaz del objeto.</span><span class="sxs-lookup"><span data-stu-id="44dc7-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="44dc7-128">La implementación actual de TNEF solo admite los identificadores IID_IMessage, IID_IStorage y IID_Istream interfaz.</span><span class="sxs-lookup"><span data-stu-id="44dc7-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="44dc7-129">El tamaño del identificador de interfaz se incluye en el tamaño de valor.</span><span class="sxs-lookup"><span data-stu-id="44dc7-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="44dc7-130">Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT_OBJECT y un identificador de interfaz de IID_Imessage), los datos del valor se codifican como una secuencia TNEF incrustada.</span><span class="sxs-lookup"><span data-stu-id="44dc7-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="44dc7-131">La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF para la secuencia original y procesando la secuencia en línea.</span><span class="sxs-lookup"><span data-stu-id="44dc7-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

