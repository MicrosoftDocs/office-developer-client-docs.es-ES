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
  
La API de replicación proporciona la funcionalidad necesaria para que un proveedor de almacén de mensajes MAPI sincronice los elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local basado en un archivo. pst privado que se crea para ese proveedor. 
  
> [!NOTE]
> Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación siguiendo las instrucciones que se indican en [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md). El proveedor solo debe usar la API en un almacén personal creado para sí mismo, y no en almacenes personales creados para otros proveedores, ya que los almacenes personales creados para otros proveedores pueden haber configurado sus propios mecanismos de replicación con el servidor correspondiente. Por ejemplo, un archivo de carpetas sin conexión (. OST) mantiene su propia relación de replicación con un servidor de Microsoft Exchange. 
  
Para usar la API de replicación, un proveedor de almacén de mensajes MAPI primero debe abrir y ajustar un almacén local basado en. pst llamando a **[NSTServiceEntry](nstserviceentry.md)**. A continuación, el proveedor puede usar las principales interfaces de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación. **IPSTX** se proporciona mediante consultas en [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)y **IOSTX** se proporciona mediante **[IPSTX:: GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>La interfaz IOSTX

La interfaz **IOSTX** es la interfaz principal que realiza la sincronización en la API de replicación. **IOSTX** mueve el almacén local a través de una serie de Estados, recuperando información en cada Estado sobre cambios en el almacén local, e informando al almacén local de cambios en el servidor. La API de replicación también especifica muchas estructuras de datos que admiten la sincronización. 
  
Un proveedor de almacenamiento, como cliente de esta API, usa la API de replicación para envolver el almacén local y desplazarse a través de estos Estados e insertar los cambios en el almacén local (como los cambios en la jerarquía de carpetas o la adición de nuevos elementos) al servidor y también recuperar información sobre los cambios en el servidor y la forma de proporcionarla a la interfaz **IOSTX** . La interfaz **IOSTX** adopta la sincronización de cambio incremental (ICS) que proporciona Microsoft Exchange Server. Para obtener más información acerca de ICS, consulte [criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). A través de **IOSTX**, el cliente usa ICS para supervisar y sincronizar los cambios incrementales de la jerarquía o el contenido de un almacén local. 
  
## <a name="the-ipstx-interface"></a>La interfaz IPSTX

 **IPSTX** y otras cinco interfaces * * IPSTX *n* * * que heredan de **IPSTX** proporcionan funcionalidad auxiliar que se puede usar para realizar la replicación a través de la interfaz de **IOSTX** . Por ejemplo, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** permite que el almacén local eMule el administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor. 
  
Para obtener más información acerca de las transiciones de estado durante la replicación, consulte [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>La API de replicación

La API de replicación proporciona las siguientes definiciones, tipos de datos e interfaces. Para obtener una implementación de ejemplo de un proveedor de almacenamiento para archivos de carpetas personales (PST), vea [acerca del proveedor de almacenamiento PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md).
  
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
    
- **[SINCRONIZÁNDOSE](sync.md)**
    
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
    

