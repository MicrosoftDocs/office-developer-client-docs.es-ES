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
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579462"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el acceso a la libreta de direcciones MAPI e incluye operaciones como mostrar cuadros de diálogo comunes; contenedores de apertura, mensajería a los usuarios y las listas de distribución; y realizar la resolución de nombres.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Expuestos por:  <br/> |Objetos de la libreta de direcciones  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, los proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IAddrBook  <br/> |
|Tipo de puntero:  <br/> |LPADRBOOK  <br/> |
|Modelo de transacciones:  <br/> |No se puede escribir  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Se abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para tener acceso a la entrada.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones concreto para determinar si hacen referencia al mismo objeto de la libreta de direcciones.  <br/> |
|[Aviso](iaddrbook-advise.md) <br/> |Registra un proveedor de servicio o cliente para recibir notificaciones sobre los cambios realizados en una o más entradas en la libreta de direcciones.  <br/> |
|[Desaconsejar](iaddrbook-unadvise.md) <br/> |Cancela un registro de notificación establecido anteriormente para una entrada de la libreta de direcciones.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Crea un identificador de entrada para una dirección de uso único.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Agrega a un nuevo destinatario a un contenedor de la libreta de direcciones o a la lista de destinatarios de un mensaje saliente.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Realiza la resolución de nombres, asignar los identificadores de entrada a los destinatarios en una lista de destinatarios.  <br/> |
|[Dirección](iaddrbook-address.md) <br/> |Muestra el cuadro de diálogo de la libreta de direcciones de Outlook.  <br/> |
|[Detalles](iaddrbook-details.md) <br/> |Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.  <br/> |
|**RecipOptions** <br/> | *No se admiten o documentado.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *No se admiten o documentado.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Devuelve el identificador de entrada del contenedor que se designa como la libreta de direcciones personales (PAB).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Designa un contenedor determinado como la libreta de direcciones personales (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Devuelve el identificador de entrada para el contenedor de la libreta de direcciones inicial.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Establece el contenedor especificado como el contenedor de libreta de direcciones predeterminada que inicialmente está disponible.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Devuelve una lista ordenada de los identificadores de entrada de los contenedores que se deben incluir en el proceso de resolución de nombres iniciado por el método [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Establece una nueva ruta de acceso de búsqueda en el perfil que se usa para el proceso de resolución de nombres.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

