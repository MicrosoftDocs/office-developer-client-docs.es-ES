---
title: Comparación de entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415358"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="50906-103">Comparación de entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="50906-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="50906-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50906-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50906-105">La implementación [de IABLogon::CompareEntryIDs](iablogon-compareentryids.md) del proveedor compara los identificadores de entrada de dos de los objetos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="50906-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="50906-106">MAPI llama a este método después de determinar que los dos identificadores de entrada contienen [el MAPIUID](mapiuid.md)registrado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="50906-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="50906-107">Por lo tanto, el **método CompareEntryIDs** no necesita comprobar que los identificadores de entrada pasados para los parámetros  _lpEntryID1_ y  _lpEntryID2_ pertenecen al proveedor.</span><span class="sxs-lookup"><span data-stu-id="50906-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="50906-108">Llamar **a IABLogon::CompareEntryIDs** equivale **a** recuperar la propiedad PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada uno de los dos objetos y compararlos directamente.</span><span class="sxs-lookup"><span data-stu-id="50906-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="50906-109">**Para implementar CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="50906-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="50906-110">Compruebe el tipo de los identificadores de entrada pasados si su proveedor almacena esa información.</span><span class="sxs-lookup"><span data-stu-id="50906-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="50906-111">Por ejemplo, un identificador de entrada puede pertenecer a un usuario de mensajería, mientras que el otro puede pertenecer a una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="50906-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="50906-112">Si los tipos no coinciden, establezca el contenido del parámetro  _lpulResult_ en FALSE y devuelva.</span><span class="sxs-lookup"><span data-stu-id="50906-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="50906-113">Compare los tamaños de los dos identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="50906-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="50906-114">Si no son iguales, establezca el contenido del parámetro  _lpulResult_ en FALSE y devuelva.</span><span class="sxs-lookup"><span data-stu-id="50906-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="50906-115">Compruebe que el tamaño de los identificadores de entrada es el tamaño correcto para su tipo.</span><span class="sxs-lookup"><span data-stu-id="50906-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="50906-116">Si no es así, establezca el contenido del parámetro  _lpulResult_ en FALSE y devuelva el valor de error MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="50906-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="50906-117">Compruebe si los identificadores de entrada son los mismos.</span><span class="sxs-lookup"><span data-stu-id="50906-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="50906-118">Si se comparan por igual, establezca el contenido del parámetro  _lpulResult_ en TRUE y return.</span><span class="sxs-lookup"><span data-stu-id="50906-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="50906-119">De lo contrario, esta establece en FALSE antes de volver.</span><span class="sxs-lookup"><span data-stu-id="50906-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="50906-120">Si su proveedor está comparando un identificador de entrada a corto plazo con un identificador a largo plazo, deben compararse por igual.</span><span class="sxs-lookup"><span data-stu-id="50906-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

