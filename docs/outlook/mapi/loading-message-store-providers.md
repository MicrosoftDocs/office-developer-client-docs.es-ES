---
title: Cargar proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307808"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="c30db-103">Cargar proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="c30db-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="c30db-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c30db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c30db-105">Cuando una aplicación cliente abre un almacén de mensajes, MAPI carga el archivo DLL del proveedor de almacén de mensajes en la memoria.</span><span class="sxs-lookup"><span data-stu-id="c30db-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="c30db-106">Una vez que MAPI carga el archivo DLL, se produce una secuencia muy específica de llamadas de método entre el proveedor de almacenamiento de mensajes y MAPI.</span><span class="sxs-lookup"><span data-stu-id="c30db-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="c30db-107">Esta secuencia de llamada al método habilita MAPI para obtener IMSProvider de nivel superior [: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md)y [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , y permite que el proveedor de almacén de mensajes obtenga un objeto de compatibilidad de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c30db-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="c30db-108">Después de la secuencia de llamadas, el proveedor de almacenamiento de mensajes debe estar preparado para aceptar inicios de sesión de clientes.</span><span class="sxs-lookup"><span data-stu-id="c30db-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="c30db-109">La secuencia de llamadas cuando se carga una DLL de proveedor de mensajes es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="c30db-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="c30db-110">El cliente llama a [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="c30db-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="c30db-111">Si el almacén de mensajes aún no está abierto, MAPI carga el archivo DLL del proveedor de almacenamiento y llama al punto de entrada [MSProviderInit](msproviderinit.md) del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="c30db-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="c30db-112">Si el almacén de mensajes ya está abierto, MAPI omite los pasos 2 y 3 y, a continuación, usa la interfaz [IMSProvider: IUnknown](imsprovideriunknown.md) existente para completar el paso 4.</span><span class="sxs-lookup"><span data-stu-id="c30db-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="c30db-113">**MSProviderInit** crea y devuelve un objeto **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="c30db-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="c30db-114">Llamadas MAPI [IMSProvider:: Logon](imsprovider-logon.md), pasando el identificador de entrada del almacén de mensajes de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c30db-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="c30db-115">**IMSProvider:: Logon** crea y devuelve una interfaz [IMSLogon: IUnknown](imslogoniunknown.md) y una interfaz [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) y, a continuación, llama al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) en su interfaz [IMAPISupport: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c30db-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="c30db-116">Si el identificador de entrada del almacén de mensajes del cliente hace referencia a un almacén de mensajes que ya está abierto, el proveedor de almacenamiento de mensajes puede devolver las interfaces **IMSLogon** e **IMsgStore** existentes y no necesita llamar a **AddRef** en su objeto support.</span><span class="sxs-lookup"><span data-stu-id="c30db-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="c30db-117">Si el cliente no estableció la marca MAPI_NO_MAIL cuando inició sesión y no estableció la MDB_NO_MAIL en el paso 1, MAPI proporciona el identificador de entrada del almacén de mensajes a la cola MAPI para que la cola MAPI pueda iniciar sesión en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c30db-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="c30db-118">MAPI devuelve la interfaz **IMsgStore** al cliente.</span><span class="sxs-lookup"><span data-stu-id="c30db-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="c30db-119">La cola MAPI llama a [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="c30db-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="c30db-120">**IMSProvider:: SpoolerLogon** devuelve las mismas interfaces **IMSLogon** y **IMsgStore** del paso 5.</span><span class="sxs-lookup"><span data-stu-id="c30db-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c30db-121">Si se produce un error en la llamada de inicio de sesión al proveedor del almacén de mensajes porque se proporcionó una contraseña incorrecta y el proveedor de almacenamiento de mensajes no puede mostrar una interfaz para solicitar la contraseña correcta, debe devolver MAPI_E_FAILONEPROVIDER de \*\*IMSProvider:: Logon \*\*método.</span><span class="sxs-lookup"><span data-stu-id="c30db-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="c30db-122">Esto permitirá a los clientes solicitar al usuario una contraseña para intentar iniciar sesión en el proveedor de almacenamiento de mensajes en lugar de hacer que MAPI falle para toda la sesión.</span><span class="sxs-lookup"><span data-stu-id="c30db-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c30db-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c30db-123">See also</span></span>



[<span data-ttu-id="c30db-124">Desarrollar un proveedor de almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="c30db-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

