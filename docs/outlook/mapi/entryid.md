---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816762"
---
# <a name="entryid"></a><span data-ttu-id="d907f-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d907f-103">ENTRYID</span></span>

  
  
<span data-ttu-id="d907f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d907f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d907f-105">Contiene un identificador de entrada para un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="d907f-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d907f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d907f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d907f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d907f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d907f-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="d907f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="d907f-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="d907f-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="d907f-110">Members</span><span class="sxs-lookup"><span data-stu-id="d907f-110">Members</span></span>

 <span data-ttu-id="d907f-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="d907f-111">**abFlags**</span></span>
  
> <span data-ttu-id="d907f-112">Máscara de bits de indicadores que proporcionan información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="d907f-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="d907f-113">Solo el primer byte de los indicadores, **abFlags [0]**, se puede establecer por el proveedor; los otros tres están reservados.</span><span class="sxs-lookup"><span data-stu-id="d907f-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="d907f-114">Estos marcadores no se deben establecer para los identificadores de entrada permanente; sólo se establecen para los identificadores de entrada a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="d907f-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="d907f-115">A los clientes, esta estructura es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d907f-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="d907f-116">Las siguientes marcas se pueden establecer en **abFlags [0]**:</span><span class="sxs-lookup"><span data-stu-id="d907f-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="d907f-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="d907f-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="d907f-118">El identificador de entrada no se puede usar como un destinatario de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d907f-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="d907f-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="d907f-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="d907f-120">Otros usuarios no pueden obtener acceso al identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d907f-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="d907f-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="d907f-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="d907f-122">El identificador de entrada no se puede usar en otros momentos.</span><span class="sxs-lookup"><span data-stu-id="d907f-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="d907f-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="d907f-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="d907f-124">El identificador de entrada es a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="d907f-124">The entry identifier is short-term.</span></span> <span data-ttu-id="d907f-125">Todos los otros valores de este byte deben estar establecidos a menos que se habilitan otros usos del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d907f-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="d907f-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="d907f-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="d907f-127">El identificador de entrada no se puede usar en otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="d907f-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="d907f-128">**AB**</span><span class="sxs-lookup"><span data-stu-id="d907f-128">**ab**</span></span>
  
> <span data-ttu-id="d907f-129">Indica una matriz de datos binarios que se usan en los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="d907f-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="d907f-130">La aplicación cliente no puede utilizar esta matriz.</span><span class="sxs-lookup"><span data-stu-id="d907f-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d907f-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d907f-131">Remarks</span></span>

<span data-ttu-id="d907f-132">Se utiliza la estructura de la **propiedad ENTRYID** por mensaje almacenar y proveedores para construir identificadores únicos para sus objetos de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d907f-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="d907f-133">Los identificadores de entrada se utilizan para identificar los siguientes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="d907f-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="d907f-134">Almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="d907f-134">Message stores</span></span>
    
- <span data-ttu-id="d907f-135">Folders</span><span class="sxs-lookup"><span data-stu-id="d907f-135">Folders</span></span>
    
- <span data-ttu-id="d907f-136">Mensajes</span><span class="sxs-lookup"><span data-stu-id="d907f-136">Messages</span></span>
    
- <span data-ttu-id="d907f-137">Contenedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="d907f-137">Address book containers</span></span>
    
- <span data-ttu-id="d907f-138">Listas de distribución</span><span class="sxs-lookup"><span data-stu-id="d907f-138">Distribution lists</span></span>
    
- <span data-ttu-id="d907f-139">Los usuarios de mensajería</span><span class="sxs-lookup"><span data-stu-id="d907f-139">Messaging users</span></span>
    
- <span data-ttu-id="d907f-140">Objetos de estado</span><span class="sxs-lookup"><span data-stu-id="d907f-140">Status objects</span></span>
    
- <span data-ttu-id="d907f-141">Secciones del perfil</span><span class="sxs-lookup"><span data-stu-id="d907f-141">Profile sections</span></span>
    
<span data-ttu-id="d907f-142">Cada proveedor usa un formato para la estructura de la **propiedad ENTRYID** que tenga sentido para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="d907f-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="d907f-143">Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos.</span><span class="sxs-lookup"><span data-stu-id="d907f-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="d907f-144">Para determinar si dos identificadores de entrada representan el mismo objeto, llame al método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="d907f-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="d907f-145">Cuando un cliente llama a un método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar su identificador de entrada, el objeto devuelve el formulario más permanente del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d907f-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="d907f-146">Un cliente puede comprobar que un identificador de entrada es a largo plazo mediante la comprobación de que ninguno de los indicadores se establecen en el primer byte del miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="d907f-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="d907f-147">Cuando un cliente tiene acceso a un identificador de entrada a través de una columna de una tabla, más probable es que este identificador de entrada es a corto plazo en lugar de a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="d907f-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="d907f-148">Los identificadores de entrada a corto plazo se pueden usar para abrir sus objetos correspondientes sólo en la sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="d907f-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="d907f-149">Un cliente puede comprobar que un identificador de entrada es a corto plazo mediante la comprobación de que todas las marcas se establecen en el primer byte del miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="d907f-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="d907f-150">Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="d907f-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="d907f-151">Este tipo de identificador de entrada tendrá uno o varios de los indicadores adecuados establecidos en el primer byte de su miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="d907f-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="d907f-152">Una estructura de la **propiedad ENTRYID** es similar a una estructura [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="d907f-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="d907f-153">Sin embargo, hay algunas diferencias:</span><span class="sxs-lookup"><span data-stu-id="d907f-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="d907f-154">Una estructura de la **propiedad ENTRYID** no almacena el tamaño del identificador de entrada; una estructura **FLATENTRY** lo hace.</span><span class="sxs-lookup"><span data-stu-id="d907f-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="d907f-155">Una estructura de **ENTRYID** almacena los datos de marca y el resto de los identificadores de entrada por separado; una estructura **FLATENTRY** almacena los datos de marca con el resto del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d907f-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="d907f-156">Una estructura de **ENTRYID** se pasa como parámetro a los métodos de la interfaz de [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos de **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="d907f-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="d907f-157">Una estructura de **ENTRYID** se usa para almacenar un identificador de entrada en el disco.</span><span class="sxs-lookup"><span data-stu-id="d907f-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="d907f-158">Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o páselo en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="d907f-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="d907f-159">Los clientes siempre deben pasar los identificadores de entrada alineado con naturalidad.</span><span class="sxs-lookup"><span data-stu-id="d907f-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="d907f-160">Aunque los proveedores deben administrar los identificadores de entrada arbitrariamente alineado, los clientes no deben esperar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="d907f-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="d907f-161">Error al pasar un identificador de entrada alineadas buen a un método puede causar un error de alineación en procesadores RISC.</span><span class="sxs-lookup"><span data-stu-id="d907f-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="d907f-162">El factor de alineación natural, normalmente de 8 bytes, es el tipo de datos más grande, compatible con la CPU y suele ser el mismo factor de alineación usado por el asignador de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="d907f-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="d907f-163">Una dirección de memoria con naturalidad alineado permite la CPU tener acceso a cualquier tipo de datos que admite en esa dirección sin que se genere un error de alineación.</span><span class="sxs-lookup"><span data-stu-id="d907f-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="d907f-164">Para CPU RISC, un tipo de datos de tamaño N bytes debe normalmente se alinea en un múltiplo de N bytes, con la dirección que se va a un múltiplo de N.</span><span class="sxs-lookup"><span data-stu-id="d907f-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="d907f-165">Para obtener más información, vea [Identificadores de entrada](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="d907f-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d907f-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="d907f-166">See also</span></span>



[<span data-ttu-id="d907f-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="d907f-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="d907f-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="d907f-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="d907f-169">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="d907f-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="d907f-170">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d907f-170">MAPI Structures</span></span>](mapi-structures.md)

