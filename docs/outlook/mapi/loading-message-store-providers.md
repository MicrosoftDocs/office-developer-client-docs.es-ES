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
ms.openlocfilehash: 47b209b9a8818cf235b7c28593da5778dd944989
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568703"
---
# <a name="loading-message-store-providers"></a>Cargar proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una aplicación cliente, abre un almacén de mensajes, MAPI carga el archivo DLL del proveedor de almacén de mensajes en la memoria. Después de MAPI carga el archivo DLL, se produce una secuencia muy específica de las llamadas de método entre el proveedor de almacén de mensajes y MAPI. Esta secuencia de llamada de método permite MAPI obtener el nivel superior [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), y [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) interfaces y permite que el proveedor de almacenamiento de mensajes obtener un objeto de soporte técnico MAPI. Después de la secuencia de llamada, el proveedor de almacenamiento de mensaje deberá estar preparado para aceptar los inicios de sesión de clientes. 
  
La secuencia de llamada cuando un proveedor de mensajes que se carga el archivo DLL es como sigue:
  
1. El cliente llama a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Si el almacén de mensajes no está ya abierto, MAPI carga el archivo DLL del proveedor de almacenamiento y llama a punto de entrada [MSProviderInit](msproviderinit.md) del archivo DLL. Si el almacén de mensajes ya está abierto, MAPI omite los pasos 2 y 3 y, a continuación, usa el existente [IMSProvider: IUnknown](imsprovideriunknown.md) interfaz para realizar el paso 4. 
    
3. **MSProviderInit** crea y devuelve un objeto **IMSProvider** . 
    
4. MAPI llama a [IMSProvider::Logon](imsprovider-logon.md), pasando el identificador de entrada de almacén de mensajes de la aplicación cliente.
    
5. **IMSProvider::Logon** crea y devuelve un [IMSLogon: IUnknown](imslogoniunknown.md) interfaz y un [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) de la interfaz y, a continuación, llama al método de [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) en su [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz. Si el mensaje del cliente almacena el identificador de entrada hace referencia a un almacén de mensajes que ya está abierto, el proveedor de almacenamiento de mensajes puede devolver interfaces **IMSLogon** y **IMsgStore** existentes y no es necesario llamar a **AddRef** en su objeto de soporte técnico. 
    
6. Si el cliente no ha establecido el indicador MAPI_NO_MAIL cuando inició sesión y no ha definido la MDB_NO_MAIL en el paso 1, MAPI proporciona a identificador de entrada del almacén de mensajes a la cola de MAPI para que la cola MAPI puede iniciar sesión en el almacén de mensajes.
    
7. MAPI devuelve la interfaz **IMsgStore** al cliente. 
    
8. La cola MAPI llama a [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** devuelve las mismas interfaces de **IMSLogon** y **IMsgStore** desde el paso 5. 
    
> [!NOTE]
> Si se produce un error de proveedor del almacén de la llamada de inicio de sesión para el mensaje porque se ha proporcionado una contraseña incorrecta y el proveedor de almacén de mensajes no puede mostrar una interfaz para solicitar la contraseña correcta, debe devolver MAPI_E_FAILONEPROVIDER desde el **IMSProvider::Logon **(método). Esto le permitirá a los clientes solicitar al usuario una contraseña para intentar iniciar sesión en el proveedor de almacenamiento de mensaje nuevo en lugar de lo que provoca que MAPI se lleve a cabo el proveedor para toda la sesión. 
  
## <a name="see-also"></a>Recursos adicionales



[Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

