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
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315991"
---
# <a name="entryid"></a><span data-ttu-id="cf0e9-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cf0e9-103">ENTRYID</span></span>

  
  
<span data-ttu-id="cf0e9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf0e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf0e9-105">Contiene un identificador de entrada para un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf0e9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cf0e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf0e9-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cf0e9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cf0e9-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="cf0e9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="cf0e9-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="cf0e9-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="cf0e9-110">Members</span><span class="sxs-lookup"><span data-stu-id="cf0e9-110">Members</span></span>

 <span data-ttu-id="cf0e9-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="cf0e9-111">**abFlags**</span></span>
  
> <span data-ttu-id="cf0e9-112">Máscara de máscara de los marcadores que proporcionan información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="cf0e9-113">El proveedor solo puede establecer el primer byte de las marcas, **abFlags [0]**; los otros tres están reservados.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="cf0e9-114">Estas marcas no deben establecerse para los identificadores de entrada permanentes; solo se establecen para los identificadores de entrada a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="cf0e9-115">Para los clientes, esta estructura es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="cf0e9-116">Se pueden establecer los siguientes indicadores en **abFlags [0]**:</span><span class="sxs-lookup"><span data-stu-id="cf0e9-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="cf0e9-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="cf0e9-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="cf0e9-118">El identificador de entrada no puede usarse como un destinatario en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="cf0e9-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="cf0e9-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="cf0e9-120">Otros usuarios no pueden tener acceso al identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="cf0e9-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="cf0e9-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="cf0e9-122">El identificador de entrada no se puede usar en otros momentos.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="cf0e9-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="cf0e9-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="cf0e9-124">El identificador de entrada es a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-124">The entry identifier is short-term.</span></span> <span data-ttu-id="cf0e9-125">Se deben establecer todos los demás valores de este byte, a menos que estén habilitados otros usos del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="cf0e9-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="cf0e9-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="cf0e9-127">El identificador de entrada no se puede usar en otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="cf0e9-128">**listín**</span><span class="sxs-lookup"><span data-stu-id="cf0e9-128">**ab**</span></span>
  
> <span data-ttu-id="cf0e9-129">Indica una matriz de datos binarios que usan los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="cf0e9-130">La aplicación cliente no puede usar esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf0e9-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf0e9-131">Remarks</span></span>

<span data-ttu-id="cf0e9-132">El almacén de mensajes y los proveedores de libreta de direcciones usan la estructura **EntryID** para crear identificadores únicos para sus objetos.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="cf0e9-133">Los identificadores de entrada se usan para identificar los siguientes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="cf0e9-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="cf0e9-134">Almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="cf0e9-134">Message stores</span></span>
    
- <span data-ttu-id="cf0e9-135">Folders</span><span class="sxs-lookup"><span data-stu-id="cf0e9-135">Folders</span></span>
    
- <span data-ttu-id="cf0e9-136">Mensajes</span><span class="sxs-lookup"><span data-stu-id="cf0e9-136">Messages</span></span>
    
- <span data-ttu-id="cf0e9-137">Contenedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="cf0e9-137">Address book containers</span></span>
    
- <span data-ttu-id="cf0e9-138">Listas de distribución</span><span class="sxs-lookup"><span data-stu-id="cf0e9-138">Distribution lists</span></span>
    
- <span data-ttu-id="cf0e9-139">Usuarios de mensajería</span><span class="sxs-lookup"><span data-stu-id="cf0e9-139">Messaging users</span></span>
    
- <span data-ttu-id="cf0e9-140">Objetos de estado</span><span class="sxs-lookup"><span data-stu-id="cf0e9-140">Status objects</span></span>
    
- <span data-ttu-id="cf0e9-141">Secciones de perfil</span><span class="sxs-lookup"><span data-stu-id="cf0e9-141">Profile sections</span></span>
    
<span data-ttu-id="cf0e9-142">Cada proveedor utiliza un formato para la estructura **EntryID** que tiene sentido para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="cf0e9-143">Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="cf0e9-144">Para determinar si dos identificadores de entrada representan el mismo objeto, llame al método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="cf0e9-145">Cuando un cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto para recuperar su identificador de entrada, el objeto devuelve la forma más permanente del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="cf0e9-146">Un cliente puede comprobar que un identificador de entrada es de largo plazo comprobando que ninguno de los indicadores está establecido en el primer byte del miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="cf0e9-147">Cuando un cliente obtiene acceso a un identificador de entrada a través de una columna de una tabla, lo más probable es que este identificador de entrada sea a corto plazo en lugar de largo plazo.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="cf0e9-148">Los identificadores de entrada a corto plazo pueden usarse para abrir sus objetos correspondientes sólo en la sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="cf0e9-149">Un cliente puede comprobar que un identificador de entrada es de corto plazo comprobando que todas las marcas se establecen en el primer byte del miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="cf0e9-150">Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="cf0e9-151">Dicho identificador de entrada tendrá uno o más de los indicadores adecuados establecidos en el primer byte de su miembro **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="cf0e9-152">Una estructura **EntryID** se asemeja a una estructura [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="cf0e9-153">Sin embargo, hay algunas diferencias:</span><span class="sxs-lookup"><span data-stu-id="cf0e9-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="cf0e9-154">Una estructura **EntryID** no almacena el tamaño del identificador de entrada; una estructura **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="cf0e9-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="cf0e9-155">Una estructura **EntryID** almacena los datos de la marca y el resto del identificador de entrada por separado; una estructura **FLATENTRY** almacena los datos de la marca con el resto del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="cf0e9-156">Se pasa una estructura **EntryID** como parámetro a los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos **OpenEntry** : [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [IMSLogon:: OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="cf0e9-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="cf0e9-157">Se usa una estructura **EntryID** para almacenar un identificador de entrada en el disco.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="cf0e9-158">Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="cf0e9-159">Los clientes siempre deben pasar los identificadores de entrada alineados naturalmente.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="cf0e9-160">Aunque los proveedores deben controlar los identificadores de entrada alineados arbitrariamente, los clientes no deben esperar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="cf0e9-161">Si no se pasa un identificador de entrada con buena alineación a un método, se puede producir un error de alineación en los procesadores RISC.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="cf0e9-162">El factor de alineación natural, normalmente 8 bytes, es el tipo de datos más grande que admite la CPU y suele ser el mismo factor de alineación que usa el asignador de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="cf0e9-163">Una dirección de memoria muy alineada de forma natural permite que la CPU tenga acceso a cualquier tipo de datos que admite en esa dirección sin generar un error de alineación.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="cf0e9-164">Para las CPU RISC, el tipo de datos de N bytes de tamaño debe estar alineado normalmente en un múltiplo par de N bytes, donde la dirección es un múltiplo par de N.</span><span class="sxs-lookup"><span data-stu-id="cf0e9-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="cf0e9-165">Para obtener más información, consulte identificadores de [entrada](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="cf0e9-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf0e9-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf0e9-166">See also</span></span>



[<span data-ttu-id="cf0e9-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="cf0e9-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="cf0e9-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cf0e9-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="cf0e9-169">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="cf0e9-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="cf0e9-170">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="cf0e9-170">MAPI Structures</span></span>](mapi-structures.md)

