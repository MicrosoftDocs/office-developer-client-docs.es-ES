---
title: Configuración de opciones de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417346"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="803dc-103">Configuración de opciones de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="803dc-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="803dc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="803dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="803dc-105">Puede establecer tres propiedades que describen las opciones para usar la libreta de direcciones:</span><span class="sxs-lookup"><span data-stu-id="803dc-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="803dc-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="803dc-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="803dc-107">[IAddrBook::ResolveName](iaddrbook-resolvename.md) usa la propiedad PR_AB_SEARCH_PATH para determinar los contenedores que deben participar en la resolución de nombres y el orden en que deben participar. </span><span class="sxs-lookup"><span data-stu-id="803dc-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="803dc-108">Para cada contenedor de **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** llama a su [método IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="803dc-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="803dc-109">Los contenedores al principio **de PR_AB_SEARCH_PATH** se buscan antes de los contenedores al final de **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="803dc-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="803dc-110">El orden de **búsqueda en PR_AB_SEARCH_PATH** se especifica mediante una estructura [SRowSet,](srowset.md) la misma estructura que se usa para representar filas en una tabla.</span><span class="sxs-lookup"><span data-stu-id="803dc-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="803dc-111">Puede ver la ruta de acceso de búsqueda actual llamando al método [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) y cambiarla llamando al método [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md)</span><span class="sxs-lookup"><span data-stu-id="803dc-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="803dc-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="803dc-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="803dc-113">La **PR_AB_DEFAULT_DIR** es el identificador de entrada del contenedor de la libreta de direcciones que se mostrará inicialmente cuando se muestre la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="803dc-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="803dc-114">La configuración predeterminada del directorio permanece en vigor hasta que se cambia llamando al [método IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="803dc-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="803dc-115">Puede ver el directorio predeterminado llamando al [método IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="803dc-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="803dc-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="803dc-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="803dc-117">Estas tres propiedades son especiales porque no se puede trabajar con ellos mediante los métodos **IMAPIProp** estándar.</span><span class="sxs-lookup"><span data-stu-id="803dc-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="803dc-118">En su lugar, debe usar **métodos IAddrBook.**</span><span class="sxs-lookup"><span data-stu-id="803dc-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="803dc-119">Dado que ninguna de estas propiedades se puede cambiar con **IMAPIProp::SetProps**, no es necesario llamar a **IMAPIProp::SaveChanges** para realizar cambios permanentes.</span><span class="sxs-lookup"><span data-stu-id="803dc-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="803dc-120">Las modificaciones realizadas a través **de los métodos IAddrBook** se hacen efectivas inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="803dc-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="803dc-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="803dc-121">See also</span></span>



[<span data-ttu-id="803dc-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="803dc-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

