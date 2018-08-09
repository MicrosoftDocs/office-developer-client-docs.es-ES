---
title: Información sobre la API de replicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816351"
---
# <a name="about-the-replication-api"></a>Información sobre la API de replicación

  
  
**Hace referencia a**: Outlook 
  
La API de replicación proporciona la funcionalidad para un proveedor de almacén de mensajes MAPI sincronizar los elementos de Microsoft Outlook 2013 o Microsoft Outlook 2010 entre un servidor y un almacén local privado basada en .pst que se crea para ese proveedor. 
  
> [!NOTE]
> Un proveedor de almacén de mensajes MAPI debe implementar la API de replicación según las instrucciones en [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md). El proveedor debe usar la API sólo en un almacén personal creado para sí mismo y no en almacenes personales creados para otros proveedores, debido a que los almacenes de personal crean para otros proveedores es posible que ya ha configurado sus propios mecanismos de replicación con el servidor respectivo. Por ejemplo, un archivo de carpetas sin conexión (.ost) mantiene su propia relación de replicación con un servidor de Microsoft Exchange. 
  
Para usar la API de replicación, un proveedor de almacén de mensajes MAPI en primer lugar debe abrir y se ajusta a un almacén local basada en .pst mediante una llamada a **[NSTServiceEntry](nstserviceentry.md)**. El proveedor, a continuación, puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación. **IPSTX** se proporciona mediante la consulta en [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), y **IOSTX** es proporcionado por **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>La interfaz de IOSTX

La interfaz **IOSTX** es la interfaz principal que realiza la sincronización de la API de replicación. **IOSTX** mueve el almacén local a través de una serie de Estados, recuperación de información de cada estado acerca de los cambios en el almacén local, así como para informar el almacén local de los cambios realizados en el servidor. La API de replicación especifica también muchas de las estructuras de datos que admiten la sincronización. 
  
Un proveedor de almacenamiento, como un cliente a esta API, usa la API de replicación para ajustar el almacén local y mover a través de estos Estados, e inserta los cambios en el almacén local (por ejemplo, los cambios en la jerarquía de carpetas o la adición de nuevos elementos) para el servidor y también recuperar información acerca de los cambios en el servidor y proporcionar esa información a la interfaz **IOSTX** . La interfaz de **IOSTX** adopta la sincronización de cambio Incremental (ICS) proporcionado por Microsoft Exchange Server. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx). A través de **IOSTX**, el cliente utiliza ICS para supervisar y sincronizar los cambios incrementales en la jerarquía o el contenido en un almacén local. 
  
## <a name="the-ipstx-interface"></a>La interfaz de IPSTX

 **IPSTX** y cinco otro ** IPSTX *n* ** las interfaces que heredan de **IPSTX** proporcionan funciones auxiliares que se pueden usar al realizar la replicación a través de la interfaz **IOSTX** . Por ejemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permite que el almacén local emular al administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor. 
  
Para obtener más información acerca de las transiciones de estado durante la replicación, vea [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>La API de replicación

La API de replicación proporciona las definiciones, tipos de datos e interfaces siguientes. Para una implementación de ejemplo de un proveedor de almacén de archivos de carpetas personales (PST) ajustados, vea [Acerca de ejemplo ajustado PST almacenar proveedor](about-the-sample-wrapped-pst-store-provider.md).
  
Definiciones:
  
- [Constantes de la API de replicación](mapi-constants.md)
    
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
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[ESTADO DE SINCRONIZACIÓN](syncstate.md)**
    
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
    

