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
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307808"
---
# <a name="loading-message-store-providers"></a>Cargar proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando una aplicación cliente abre un almacén de mensajes, MAPI carga la DLL del proveedor del almacén de mensajes en la memoria. Después de que MAPI carga el DLL, se produce una secuencia muy específica de llamadas a métodos entre el proveedor del almacén de mensajes y MAPI. Esta secuencia de llamadas de método permite a MAPI obtener imsprovider de nivel superior [: IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)y [IMsgStore : interfaces IMAPIProp,](imsgstoreimapiprop.md) y permite al proveedor del almacén de mensajes obtener un objeto de soporte mapi. Después de la secuencia de llamadas, el proveedor del almacén de mensajes debe estar listo para aceptar los inicios de sesión de los clientes. 
  
La secuencia de llamadas cuando se carga una DLL del proveedor de mensajes es la siguiente:
  
1. El cliente llama [a IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).
    
2. Si el almacén de mensajes aún no está abierto, MAPI carga el DLL del proveedor de almacenamiento y llama al punto de entrada [MSProviderInit](msproviderinit.md) de la DLL. Si el almacén de mensajes ya está abierto, MAPI omite los pasos 2 y 3 y, a continuación, usa la interfaz [IMSProvider : IUnknown](imsprovideriunknown.md) existente para completar el paso 4. 
    
3. **MSProviderInit** crea y devuelve un **objeto IMSProvider.** 
    
4. MAPI llama a [IMSProvider::Logon](imsprovider-logon.md), pasando el identificador de entrada del almacén de mensajes de la aplicación cliente.
    
5. **IMSProvider::Logon** crea y devuelve una interfaz [IMSLogon : IUnknown](imslogoniunknown.md) y una [interfaz IMsgStore : IMAPIProp](imsgstoreimapiprop.md) y, a continuación, llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) en su [interfaz IMAPISupport : IUnknown.](imapisupportiunknown.md) Si el identificador de entrada del almacén de mensajes del cliente hace referencia a un almacén de mensajes que ya está abierto, el proveedor del almacén de mensajes puede devolver las interfaces **IMSLogon** e **IMsgStore** existentes y no necesita llamar a **AddRef** en su objeto de soporte técnico. 
    
6. Si el cliente no estableció la marca MAPI_NO_MAIL cuando inició sesión y no estableció el MDB_NO_MAIL en el paso 1, MAPI proporciona el identificador de entrada del almacén de mensajes a la cola MAPI para que la cola MAPI pueda iniciar sesión en el almacén de mensajes.
    
7. MAPI devuelve la **interfaz IMsgStore** al cliente. 
    
8. La cola MAPI llama a [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).
    
9. **IMSProvider::SpoolerLogon** devuelve las mismas interfaces **IMSLogon** e **IMsgStore** del paso 5. 
    
> [!NOTE]
> Si se produce un error en la llamada de inicio de sesión al proveedor del almacén de mensajes porque se proporcionó una contraseña incorrecta y el proveedor del almacén de mensajes no puede mostrar una interfaz para solicitar la contraseña correcta, debe devolver MAPI_E_FAILONEPROVIDER del método **IMSProvider::Logon.** Esto permitirá que los clientes soliciten al usuario una contraseña para intentar iniciar sesión de nuevo en el proveedor del almacén de mensajes en lugar de provocar que MAPI falle al proveedor durante toda la sesión. 
  
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

