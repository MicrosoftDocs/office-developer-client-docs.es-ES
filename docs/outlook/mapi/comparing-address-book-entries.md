---
title: Comparación de entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816551"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="bf086-103">Comparación de entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="bf086-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="bf086-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf086-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf086-105">[IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementación de su proveedor compara los identificadores de entrada para dos de los objetos de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="bf086-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="bf086-106">MAPI llama a este método después de determinar que los identificadores de dos entrada contienen su proveedor había registrado [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="bf086-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="bf086-107">Por lo tanto, el método **CompareEntryIDs** no necesita verificar que los identificadores de entrada que se pasó para los parámetros _lpEntryID1_ y _lpEntryID2_ pertenecen a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="bf086-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="bf086-108">Al llamar a **IABLogon::CompareEntryIDs** es equivalente a la recuperación de la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada uno de los dos objetos y su comparación directamente.</span><span class="sxs-lookup"><span data-stu-id="bf086-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="bf086-109">**Para implementar CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="bf086-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="bf086-110">Comprobar el tipo de los identificadores de entrada que se pasó si su proveedor almacena esa información.</span><span class="sxs-lookup"><span data-stu-id="bf086-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="bf086-111">Por ejemplo, un identificador de entrada es posible que pertenecen a un usuario de mensajería mientras la otra es posible que pertenecen a una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="bf086-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="bf086-112">Si los tipos no coinciden, establezca el contenido del parámetro _lpulResult_ en FALSE y devolución.</span><span class="sxs-lookup"><span data-stu-id="bf086-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="bf086-113">Compare los tamaños de los identificadores de dos entrada.</span><span class="sxs-lookup"><span data-stu-id="bf086-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="bf086-114">Si no son las mismas, establezca el contenido del parámetro _lpulResult_ en FALSE y devolver.</span><span class="sxs-lookup"><span data-stu-id="bf086-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="bf086-115">Compruebe que el tamaño de los identificadores de entrada es el tamaño correcto para su tipo.</span><span class="sxs-lookup"><span data-stu-id="bf086-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="bf086-116">Si no es así, Establece el contenido del parámetro _lpulResult_ en FALSE y devolver el valor de error MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="bf086-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="bf086-117">Compruebe si los identificadores de entrada son los mismos.</span><span class="sxs-lookup"><span data-stu-id="bf086-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="bf086-118">Si se comparan igualmente, establezca el contenido del parámetro _lpulResult_ en TRUE y devolución.</span><span class="sxs-lookup"><span data-stu-id="bf086-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="bf086-119">De lo contrario, establézcalo en FALSE antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="bf086-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="bf086-120">Si su proveedor es comparar un identificador de entrada a corto plazo con un identificador a largo plazo, debe comparar igualmente.</span><span class="sxs-lookup"><span data-stu-id="bf086-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

