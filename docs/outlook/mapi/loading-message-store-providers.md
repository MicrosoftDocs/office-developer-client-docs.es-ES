---
title: Cargar proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 96e2ca38391931508dd9f3f78f3ba69e6f8b9c15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818030"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="b00ee-103">Cargar proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="b00ee-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="b00ee-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b00ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b00ee-105">Cuando una aplicación cliente, abre un almacén de mensajes, MAPI carga el archivo DLL del proveedor de almacén de mensajes en la memoria.</span><span class="sxs-lookup"><span data-stu-id="b00ee-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="b00ee-106">Después de MAPI carga el archivo DLL, se produce una secuencia muy específica de las llamadas de método entre el proveedor de almacén de mensajes y MAPI.</span><span class="sxs-lookup"><span data-stu-id="b00ee-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="b00ee-107">Esta secuencia de llamada de método permite MAPI obtener el nivel superior [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), y [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces y permite que el proveedor de almacenamiento de mensajes obtener un objeto de soporte técnico MAPI.</span><span class="sxs-lookup"><span data-stu-id="b00ee-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="b00ee-108">Después de la secuencia de llamada, el proveedor de almacenamiento de mensaje deberá estar preparado para aceptar los inicios de sesión de clientes.</span><span class="sxs-lookup"><span data-stu-id="b00ee-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="b00ee-109">La secuencia de llamada cuando un proveedor de mensajes que se carga el archivo DLL es como sigue:</span><span class="sxs-lookup"><span data-stu-id="b00ee-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="b00ee-110">El cliente llama a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="b00ee-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="b00ee-111">Si el almacén de mensajes no está ya abierto, MAPI carga el archivo DLL del proveedor de almacenamiento y llama a punto de entrada [MSProviderInit](msproviderinit.md) del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b00ee-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="b00ee-112">Si el almacén de mensajes ya está abierto, MAPI omite los pasos 2 y 3 y, a continuación, usa el existente [IMSProvider: IUnknown](imsprovideriunknown.md) interfaz para realizar el paso 4.</span><span class="sxs-lookup"><span data-stu-id="b00ee-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="b00ee-113">**MSProviderInit** crea y devuelve un objeto **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="b00ee-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="b00ee-114">MAPI llama a [IMSProvider::Logon](imsprovider-logon.md), pasando el identificador de entrada de almacén de mensajes de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b00ee-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="b00ee-115">**IMSProvider::Logon** crea y devuelve un [IMSLogon: IUnknown](imslogoniunknown.md) interfaz y un [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) de la interfaz y, a continuación, llama al método de [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) en su [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="b00ee-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="b00ee-116">Si el mensaje del cliente almacena el identificador de entrada hace referencia a un almacén de mensajes que ya está abierto, el proveedor de almacenamiento de mensajes puede devolver interfaces **IMSLogon** y **IMsgStore** existentes y no es necesario llamar a **AddRef** en su objeto de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="b00ee-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="b00ee-117">Si el cliente no ha establecido el indicador MAPI_NO_MAIL cuando inició sesión y no ha definido la MDB_NO_MAIL en el paso 1, MAPI proporciona a identificador de entrada del almacén de mensajes a la cola de MAPI para que la cola MAPI puede iniciar sesión en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b00ee-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="b00ee-118">MAPI devuelve la interfaz **IMsgStore** al cliente.</span><span class="sxs-lookup"><span data-stu-id="b00ee-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="b00ee-119">La cola MAPI llama a [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="b00ee-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="b00ee-120">**IMSProvider::SpoolerLogon** devuelve las mismas interfaces de **IMSLogon** y **IMsgStore** desde el paso 5.</span><span class="sxs-lookup"><span data-stu-id="b00ee-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b00ee-121">Si se produce un error de proveedor del almacén de la llamada de inicio de sesión para el mensaje porque se ha proporcionado una contraseña incorrecta y el proveedor de almacén de mensajes no puede mostrar una interfaz para solicitar la contraseña correcta, debe devolver MAPI_E_FAILONEPROVIDER desde el **IMSProvider::Logon **(método).</span><span class="sxs-lookup"><span data-stu-id="b00ee-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="b00ee-122">Esto le permitirá a los clientes solicitar al usuario una contraseña para intentar iniciar sesión en el proveedor de almacenamiento de mensaje nuevo en lugar de lo que provoca que MAPI se lleve a cabo el proveedor para toda la sesión.</span><span class="sxs-lookup"><span data-stu-id="b00ee-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b00ee-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b00ee-123">See also</span></span>



[<span data-ttu-id="b00ee-124">Desarrollar un proveedor de almac�n de mensajes de MAPI</span><span class="sxs-lookup"><span data-stu-id="b00ee-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

