---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341380"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el acceso a la libreta de direcciones MAPI e incluye operaciones como mostrar cuadros de diálogo comunes; abrir contenedores, usuarios de mensajería y listas de distribución; y la resolución de nombres.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
|Expuesto por:  <br/> |Objetos de la libreta de direcciones  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IAddrBook  <br/> |
|Tipo de puntero:  <br/> |LPADRBOOK  <br/> |
|Modelo de transacción:  <br/> |No se puede escribir  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que puede usarse para tener acceso a la entrada.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones determinado para determinar si hacen referencia al mismo objeto de la libreta de direcciones.  <br/> |
|[Aconsej](iaddrbook-advise.md) <br/> |Registra un cliente o un proveedor de servicios para recibir notificaciones sobre los cambios en una o más entradas de la libreta de direcciones.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Cancela un registro de notificaciones previamente establecido para una entrada de la libreta de direcciones.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crea un identificador de entrada para una dirección de uso único.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Agrega un nuevo destinatario a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Realiza la resolución de nombres, asignando identificadores de entrada a los destinatarios de una lista de destinatarios.  <br/> |
|[Address](iaddrbook-address.md) <br/> |Muestra el cuadro de diálogo libreta de direcciones de Outlook.  <br/> |
|[Detalles](iaddrbook-details.md) <br/> |Muestra un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones en particular.  <br/> |
|**RecipOptions** <br/> | *No es compatible o documentado.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *No es compatible o documentado.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Devuelve el identificador de entrada del contenedor que se ha designado como la libreta personal de direcciones (PAB).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Designa un contenedor determinado como la libreta personal de direcciones (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Devuelve el identificador de entrada del contenedor de libreta de direcciones inicial.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Establece el contenedor especificado como el contenedor de libreta de direcciones predeterminado que se pone a disposición del principio.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Devuelve una lista ordenada de identificadores de entrada de los contenedores que se incluirán en el proceso de resolución de nombres Iniciado por el método [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Establece una nueva ruta de búsqueda en el perfil que se usa para el proceso de resolución de nombres.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

