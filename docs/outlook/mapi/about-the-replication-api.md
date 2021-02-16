---
title: Información sobre la API de replicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329522"
---
# <a name="about-the-replication-api"></a>Información sobre la API de replicación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de replicación proporciona la funcionalidad de un proveedor de almacén de mensajes MAPI para sincronizar elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local privado basado en .pst que se crea para ese proveedor. 
  
> [!NOTE]
> Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación de acuerdo con las instrucciones de [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md). El proveedor debe usar la API solo en un almacén personal creado para sí mismo y no en almacenes personales creados para otros proveedores, porque es posible que los almacenes personales creados para otros proveedores ya tengan configurados sus propios mecanismos de replicación con el servidor respectivo. Por ejemplo, un archivo de carpetas sin conexión (.ost) mantiene su propia relación de replicación con un servidor de Microsoft Exchange. 
  
Para usar la API de replicación, un proveedor de almacén de mensajes MAPI primero debe abrir y encapsular un almacén local basado en .pst llamando a **[NSTServiceEntry](nstserviceentry.md)**. A continuación, el proveedor puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** e **[IPSTX,](ipstxiunknown.md)** para llevar a cabo la replicación. **IPSTX** se proporciona consultando en [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)y **IOSTX** lo proporciona **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>Interfaz IOSTX

La **interfaz IOSTX** es la interfaz principal que realiza la sincronización en la API de replicación. **IOSTX** mueve el almacén local a través de una serie de estados, recuperando información en cada estado sobre los cambios en el almacén local, así como informando al almacén local de los cambios en el servidor. La API de replicación también especifica muchas estructuras de datos que admiten la sincronización. 
  
Un proveedor de almacén, como cliente de esta API, usa la API de replicación para encapsular el almacén local y desplazarse por estos estados, insertar los cambios en el almacén local (como los cambios en la jerarquía de carpetas o la adición de nuevos elementos) en el servidor, y también recuperar información sobre los cambios en el servidor y proporcionar esa información a la interfaz **IOSTX.** La **interfaz IOSTX** adopta la sincronización de cambios incremental (ICS) proporcionada por Microsoft Exchange Server. Para obtener más información acerca de ICS, vea [Criterios de evaluación de ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx) Mediante **IOSTX,** el cliente usa ICS para supervisar y sincronizar los cambios incrementales en la jerarquía o el contenido de un almacén local. 
  
## <a name="the-ipstx-interface"></a>Interfaz IPSTX

 **IPSTX** y otras cinco interfaces **IPSTX *n* ** que heredan de **IPSTX** proporcionan funcionalidad auxiliar que se puede usar al realizar la replicación a través de la interfaz **IOSTX.** Por ejemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** le permite hacer que el almacén local emule el Administrador de protocolo de Outlook para colar mensajes salientes en un servidor. 
  
Para obtener más información acerca de las transiciones de estado durante la replicación, vea [Acerca de la máquina de estado de replicación.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>API de replicación

La API de replicación proporciona las siguientes definciones, tipos de datos e interfaces. Para obtener una implementación de ejemplo de un proveedor de almacenamiento para archivos de carpetas personales ajustados (PST), consulte Acerca del [proveedor de almacén de ARCHIVOS PST ajustados de ejemplo.](about-the-sample-wrapped-pst-store-provider.md)
  
Definiciones:
  
- [Constantes para la API de replicación](mapi-constants.md)
    
Funciones:
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Tipos de datos:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[Sincronizar](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Interfaces:
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

