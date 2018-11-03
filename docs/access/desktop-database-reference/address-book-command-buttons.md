---
title: Botones de comando de la libreta de direcciones
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f586b92f309ffd330230bf732d0e477acf0a8ba9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946933"
---
# <a name="address-book-command-buttons"></a>Botones de comando de la libreta de direcciones


**Se aplica a**: Access 2013, Office 2013


La aplicación Libreta de direcciones incluye los siguientes botones de comando:

- Un botón **Buscar** para enviar una consulta a la base de datos.

- Un botón **Borrar** para borrar los cuadros de texto antes de iniciar una nueva búsqueda.

- Un botón **Actualizar perfil** para guardar los cambios de un registro de empleado.

- Un botón **Cancelar cambios** para descartar cambios.

## <a name="find-button"></a>Botón Buscar

Al hacer clic en el botón **Buscar** , se activa la búsqueda de VBScript\_procedimiento OnClick Sub, que genera y envía la consulta SQL. Al hacer clic en este botón, se rellena la cuadrícula de datos.

## <a name="building-the-sql-query"></a>Generar la consulta SQL

La primera parte de la búsqueda\_procedimiento OnClick Sub basa la consulta SQL, una frase a la vez, anexando cadenas de texto a una instrucción SELECT de SQL global. Comienza estableciendo la variable en una instrucción SELECT de SQL que solicita todas las filas de datos de la tabla de origen de datos. A continuación, el subprocedimiento examina cada uno de los cuatro cuadros de entrada de la página.

Dado que el programa utiliza la palabra en la creación de las instrucciones SQL, las consultas son búsquedas de subcadenas, en vez de coincidencias exactas.

Por ejemplo, si **el cuadro** LastName contenía la entrada "Berge" y el cuadro **Title** la entrada "Program Manager", la instrucción SQL (valor) será:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Si la consulta obtuvo resultados, todas las personas cuyo apellido contiene el texto "Berge" (tales como Berge y Berger) y cuyo título o cargo contiene las palabras "Program Manager" (por ejemplo, Program Manager, Advanced Technologies) aparecerán en la cuadrícula de datos HTML.

## <a name="preparing-and-sending-the-query"></a>Preparar y enviar la consulta

La última parte de la búsqueda\_procedimiento OnClick Sub consta de dos instrucciones. La primera instrucción asigna a la propiedad SQL del objeto RDS.DataControl la consulta SQL generada dinámicamente. La segunda instrucción hace que el **RDS. DataControl** () para consultar la base de datos de objetos y, a continuación, muestre los nuevos resultados de la consulta en la cuadrícula.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Botón Actualizar perfil

Al hacer clic en el botón **Actualizar perfil** , se activa la actualización de VBScript\_procedimiento OnClick Sub, que se ejecuta el objeto RDS. Métodos de SubmitChanges y Refresh de () del objeto DataControl.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Cuando DC1. Ejecuta SubmitChanges, el servicio de datos remoto empaqueta toda la información de actualización y se envía al servidor a través de HTTP. La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado. , el servicio de datos remotos (RDS) empaqueta toda la información de actualización y la envía al servidor mediante HTTP. La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado. DC1. Refresh no es necesario después de **SubmitChanges** con RDS, pero garantiza datos actualizados.

## <a name="cancel-changes-button"></a>Botón Cancelar cambios

Al hacer clic en **Cancelar cambios** , se activa la cancelación de VBScript\_procedimiento OnClick Sub, que se ejecuta el objeto RDS. Del objeto DataControl (método CancelUpdate.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Cuando se ejecuta, éste descarta cualquier modificación que ha realizado un usuario en un registro de empleado en la cuadrícula de datos desde la última consulta o actualización. Restaura los valores originales.

