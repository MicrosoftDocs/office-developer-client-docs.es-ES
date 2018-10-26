---
title: Abrir la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 62a4e6a09570cc3d71b0797ed7fff162d05ee416
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583690"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="a2251-103">Abrir la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="a2251-103">Opening the address book</span></span>

<span data-ttu-id="a2251-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2251-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span><span class="sxs-lookup"><span data-stu-id="a2251-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="a2251-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span><span class="sxs-lookup"><span data-stu-id="a2251-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="a2251-p103">Los clientes no interactivos deben omitir la advertencia y continuar como si el m�todo se realiz� correctamente. La interfaz devuelta **IAddrBook** es v�lida independientemente de si todos, algunos o ninguno de los proveedores de libreta de direcciones en el perfil se est�n ejecutando. Por lo tanto, los clientes tanto interactivos y siempre deben recordar liberar el puntero **IAddrBook** cuando finaliza la sesi�n.</span><span class="sxs-lookup"><span data-stu-id="a2251-p103">Noninteractive clients should ignore the warning and proceed as if the method succeeded. The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running. Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

