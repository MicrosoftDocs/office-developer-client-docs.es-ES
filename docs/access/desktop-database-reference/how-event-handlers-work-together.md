---
title: Cómo funcionan conjuntamente los controladores de eventos
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a926bed97cf3f21e81fbf01eae554aaec45406a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947787"
---
# <a name="how-event-handlers-work-together"></a>Cómo funcionan conjuntamente los controladores de eventos

**Se aplica a**: Access 2013, Office 2013

A menos que se programe en Visual Basic, todos los controladores de eventos **Connection** y **Recordset** deben estar implementados, independientemente de que se procesen realmente todos los eventos. La cantidad de trabajo que implica la implementación depende del lenguaje de programación. Para obtener más información, vea [ Creación de instancias de eventos de ADO por lenguaje ](https://msdn.microsoft.com/library/jj250244\(v=office.15\)).

## <a name="paired-event-handlers"></a>Controladores de eventos emparejados

Cada controlador de eventos Will tiene asociado un controlador de eventos Complete. Por ejemplo, cuando una aplicación cambia el valor de un campo, se llama al controlador de eventos **WillChangeField**. Si el cambio es aceptable, la aplicación no modifica el parámetro **adStatus** y se lleva a cabo la operación. Cuando finaliza la operación, un evento **FieldChangeComplete** notifica a la aplicación la finalización de la operación. Si ésta ha finalizado correctamente, **adStatus** contiene **adStatusOK**; en caso contrario, **adStatus** contiene **adStatusErrorsOccurred** y es preciso comprobar el objeto **Error** para determinar la causa del error.

Cuando se llama a **WillChangeField**, es posible que se determine que no se debió realizar el cambio. En ese caso, establezca el valor de **adStatus** en **adStatusCancel**. Se cancela la operación y el evento **FieldChangeComplete** recibe para **adStatus** el valor **adStatusErrorsOccurred**. El objeto **Error** contiene **adErrOperationCancelled** para que el controlador **FieldChangeComplete** sepa que se canceló la operación. Sin embargo, es preciso comprobar el valor del parámetro **adStatus** antes de cambiarlo, porque establecer el valor de **adStatus** en **adStatusCancel** no tiene ningún efecto si el parámetro se estableció en **adStatusCantDeny** al iniciarse el procedimiento.

A veces, una operación puede producir varios eventos. Por ejemplo, el objeto **Recordset** tiene eventos emparejados para los cambios de **Field** y **Record**. Cuando la aplicación cambia el valor de un **Field**, se llama al controlador de eventos **WillChangeField**. Si determina que la operación puede continuar, también se llamará al controlador de eventos **WillChangeRecord**. Si este controlador permite asimismo que continúe el evento, se realiza el cambio y se llama a los controladores de eventos **FieldChangeComplete** y **RecordChangeComplete**. El orden en que se llama a los controladores de eventos Will para una determinada operación no está definido, por lo que debe evitarse escribir código que requiera que se llame a los controladores de eventos en una secuencia determinada.

En los casos en los que se provocan varios eventos Will, es posible que uno de los eventos cancele la operación que está pendiente. Por ejemplo, cuando la aplicación cambia el valor de un **Field**, normalmente se llama tanto al controlador de eventos **WillChangeField** como al controlador de eventos **WillChangeRecord**. Sin embargo, si se cancela la operación en el primer controlador de eventos, se llama inmediatamente a su controlador Complete asociado con **adStatusOperationCancelled**. No se llama nunca al segundo controlador. Sin embargo, si el primer controlador de eventos permite que el evento continúe, se llamará al otro controlador de eventos. Si cancela la operación, se llamará a ambos eventos Complete como en los ejemplos anteriores.

## <a name="unpaired-event-handlers"></a>Controladores de eventos no emparejados

Siempre y cuando el estado pasado al evento no **sea adStatusCantDeny**, puede desactivar las notificaciones de eventos para cualquier evento devolviendo **adStatusUnwantedEvent** en el parámetro *Status* . Por ejemplo, cuando se llama la primera vez al controlador de eventos Complete, puede devolver **adStatusUnwantedEvent**. Posteriormente, recibirá sólo los eventos Will. Sin embargo, algunos eventos pueden desencadenarse por varias razones. En ese caso, el evento tendrá un parámetro de *motivo* . Si devuelve **adStatusUnwantedEvent**, dejará de recibir notificaciones de ese evento sólo si se produce por ese motivo concreto. Es decir, recibirá notificaciones por cada razón por la que se puede desencadenar el evento.

Los controladores de eventos Will pueden ser útiles cuando desea examinar los parámetros que se van a utilizar en una operación. Puede modificar esos parámetros de operación o cancelar la operación.

Como alternativa, deje habilitada la notificación de eventos Complete. Cuando se llame al primer controlador de eventos Will, devuelva **adStatusUnwantedEvent**. Posteriormente, sólo recibirá los eventos Complete.

Los controladores de eventos Complete pueden ser útiles para administrar las operaciones asincrónicas. Cada operación asincrónica tiene un evento Complete correspondiente.

Por ejemplo, puede que tarde mucho tiempo en rellenar un objeto [Recordset](recordset-object-ado.md) de gran tamaño. Si la aplicación se ha escrito correctamente, puede iniciar una operación y continuar con otros procesamientos. Finalmente notificará cuando se rellena el **conjunto de registros** por un evento **ExecuteComplete** .

## <a name="single-event-handlers-and-multiple-objects"></a>Un solo controlador de eventos y varios objetos

La flexibilidad de un lenguaje de programación como Microsoft Visual C++ permite que un controlador de eventos procese los eventos de varios objetos. Por ejemplo, un controlador de eventos **Disconnect** puede procesar los eventos de varios objetos **Connection**. Si una de las conexiones finaliza, se llamará al controlador de eventos **Disconnect**. Se podrá indicar cuál es la conexión que ha causado el evento porque el parámetro de objeto del controlador de eventos estará establecido en el correspondiente objeto **Connection**.


> [!NOTE]
> <P>[!NOTA] Esta técnica no se puede utilizar en Visual Basic porque este lenguaje sólo puede correlacionar un objeto con un controlador de eventos.</P>


