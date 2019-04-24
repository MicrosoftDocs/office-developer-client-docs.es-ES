---
title: Anticipación de errores
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4bd130ca05527c7761ca587781c1fd4f939ebe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297175"
---
# <a name="anticipating-errors"></a>Anticipación de errores


**Se aplica a:** Access 2013, Office 2013

La prevención de errores es tan importante como el tratamiento de éstos. Esta última sección contiene una breve lista de medidas de precaución que se pueden adoptar en la aplicación para reducir la probabilidad de que se produzcan errores.

Compruebe el estado de los objetos observando el valor de la propiedad **State** antes de intentar realizar una operación que utilice esos objetos. Por ejemplo, si su aplicación utiliza una **conexión** global, compruebe su propiedad **State** para ver si está abierta antes de llamar al método **Open**.

- Cualquier programa que acepte datos de un usuario debe incluir código para validar esos datos antes de enviarlos al almacén de datos. No puede confiar en que el almacén de datos, ni el proveedor, ni ADO, y ni siquiera el lenguaje de programación, le notificarán los problemas. Debe revisar cada byte que introduzcan los usuarios y comprobar que los datos son del tipo correcto para el campo correspondiente y que los campos obligatorios no están vacíos.

Compruebe los datos antes de intentar escribirlos en el almacén de datos. La forma más sencilla de hacerlo es controlar los eventos **WillMove** o **WillUpdateRecordset**. Para obtener una descripción más completa de cómo controlar los eventos de ADO, vea [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md).

Asegúrese de que los objetos **Recordset** no se salen de los límites del **conjunto de registros** antes de intentar mover el puntero de registros. Si trata de **desplazarse al siguiente** cuando **EOF** es True o **desplazarse al anterior** cuando **BOF** es True, se producirá un error. Si ejecuta cualquiera de los métodos **Move** cuando tanto **EOF** como **BOF** son True, se producirá un error.

También se producirán errores si intenta realizar operaciones como **Seek** y **Find** en un **conjunto de registros** vacío.

