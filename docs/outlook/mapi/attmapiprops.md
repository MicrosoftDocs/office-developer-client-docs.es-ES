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
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816460"
---
# <a name="attmapiprops"></a><span data-ttu-id="96e7c-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="96e7c-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="96e7c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96e7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96e7c-105">El atributo **attMAPIProps** es especial en que se puede usar para codificar cualquier propiedad MAPI que no tiene un equivalente en el conjunto de atributos definidas por el TNEF existentes.</span><span class="sxs-lookup"><span data-stu-id="96e7c-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="96e7c-106">Los datos del atributo están un conjunto contado de las propiedades MAPI que distribuyen un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="96e7c-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="96e7c-107">El formato de codificación, lo cual permite cualquier conjunto de propiedades MAPI, que es como sigue:</span><span class="sxs-lookup"><span data-stu-id="96e7c-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="96e7c-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="96e7c-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="96e7c-109">propiedad count _Property_Value..._</span><span class="sxs-lookup"><span data-stu-id="96e7c-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="96e7c-110">Debe haber tantos elementos _Property_Value_ tal y como indica el valor de la propiedad count.</span><span class="sxs-lookup"><span data-stu-id="96e7c-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="96e7c-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="96e7c-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="96e7c-112">etiqueta de la propiedad _Property_property etiqueta _Proptag_Name (propiedad)_</span><span class="sxs-lookup"><span data-stu-id="96e7c-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="96e7c-113">La etiqueta de propiedad es simplemente el valor asociado con el identificador de la propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96e7c-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="96e7c-114">_Propiedad:_</span><span class="sxs-lookup"><span data-stu-id="96e7c-114">_Property:_</span></span>
  
>  <span data-ttu-id="96e7c-115">Valor-recuento de _valor_ _valor..._</span><span class="sxs-lookup"><span data-stu-id="96e7c-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="96e7c-116">_Valor:_</span><span class="sxs-lookup"><span data-stu-id="96e7c-116">_Value:_</span></span>
  
> <span data-ttu-id="96e7c-117">datos de valor valor tamaño-datos de valor espaciado espaciado interno de datos del valor de tamaño de valor valor-IID</span><span class="sxs-lookup"><span data-stu-id="96e7c-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="96e7c-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="96e7c-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="96e7c-119">relleno de nombre guid nombre del identificador de nombre de tipo de nombre-guid nombre tipo longitud de la cadena de nombre de la cadena de nombre</span><span class="sxs-lookup"><span data-stu-id="96e7c-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="96e7c-120">La encapsulación de cada propiedad varía según el tipo de propiedad y el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="96e7c-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="96e7c-121">Tipos, identificadores y etiquetas de propiedad se definen en los archivos de encabezado Mapitags.h y Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="96e7c-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="96e7c-122">Si la propiedad es una propiedad con nombre, a continuación, la etiqueta de propiedad es seguida por el nombre de la propiedad MAPI, formado por un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="96e7c-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="96e7c-123">Propiedades multivalor y las propiedades con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o pt Object, se tratan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="96e7c-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="96e7c-124">En primer lugar el número de valores, que se codifica como un 32-bit sin firmar durante cuánto tiempo, se coloca en la secuencia TNEF, seguida de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="96e7c-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="96e7c-125">Datos del valor de la propiedad se codifican como su tamaño en bytes seguido de los datos de valor propio.</span><span class="sxs-lookup"><span data-stu-id="96e7c-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="96e7c-126">Los datos del valor se rellenen hasta un límite de 4 bytes, aunque no se incluye la cantidad de relleno en el tamaño del valor.</span><span class="sxs-lookup"><span data-stu-id="96e7c-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="96e7c-127">Si la propiedad es de tipo pt Object, el tamaño del valor es seguido por el identificador de interfaz del objeto.</span><span class="sxs-lookup"><span data-stu-id="96e7c-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="96e7c-128">La implementación actual de TNEF sólo es compatible con los identificadores de interfaz IID_IMessage, IID_IStorage y IID_Istream.</span><span class="sxs-lookup"><span data-stu-id="96e7c-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="96e7c-129">El tamaño del identificador de interfaz se incluye en el tamaño del valor.</span><span class="sxs-lookup"><span data-stu-id="96e7c-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="96e7c-130">Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT Object y un identificador de interfaz de IID_Imessage), los datos de valor se codifican como una secuencia de TNEF incrustada.</span><span class="sxs-lookup"><span data-stu-id="96e7c-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="96e7c-131">La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF de la secuencia original y el en línea de la secuencia de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="96e7c-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

