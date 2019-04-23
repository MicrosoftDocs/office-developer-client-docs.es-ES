---
title: Botones de comando de la libreta de direcciones
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282481"
---
# <a name="address-book-command-buttons"></a>Botones de comando de la libreta de direcciones


**Se aplica a:** Access 2013, Office 2013


La aplicación Libreta de direcciones incluye los siguientes botones de comando:

- Un botón **Buscar** para enviar una consulta a la base de datos.

- Un botón **Borrar** para borrar los cuadros de texto antes de iniciar una nueva búsqueda.

- Un botón **Actualizar perfil** para guardar los cambios de un registro de empleado.

- Un botón **Cancelar cambios** para descartar cambios.

## <a name="find-button"></a>Botón Buscar

Al hacer clic en el botón **Buscar** , se\_activa el procedimiento Sub OnClick de búsqueda de VBScript, que genera y envía la consulta SQL. Al hacer clic en este botón, se rellena la cuadrícula de datos.

## <a name="building-the-sql-query"></a>Generar la consulta SQL

La primera parte del procedimiento Find\_OnClick genera la consulta SQL, una frase cada vez, anexando cadenas de texto a una instrucción SQL SELECT global. Comienza estableciendo la variable en una instrucción SELECT de SQL que solicita todas las filas de datos de la tabla de origen de datos. A continuación, el subprocedimiento examina cada uno de los cuatro cuadros de entrada de la página.

Dado que el programa utiliza la palabra en la creación de instrucciones SQL, las consultas son búsquedas de subcadenas en lugar de coincidencias exactas.

Por ejemplo, si el cuadro **Apellido** contenía la entrada "Berge" y el cuadro **title** contenía la entrada "Program Manager", la instrucción SQL (valor de) leería lo siguiente:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Si la consulta obtuvo resultados, todas las personas cuyo apellido contiene el texto "Berge" (tales como Berge y Berger) y cuyo título o cargo contiene las palabras "Program Manager" (por ejemplo, Program Manager, Advanced Technologies) aparecerán en la cuadrícula de datos HTML.

## <a name="preparing-and-sending-the-query"></a>Preparar y enviar la consulta

La última parte del procedimiento de\_la cláusula Find OnClick consta de dos instrucciones. La primera instrucción asigna a la propiedad SQL del objeto RDS.DataControl la consulta SQL generada dinámicamente. La segunda instrucción hace que el **objeto RDS. DataControl** () para consultar la base de datos y, a continuación, mostrar los nuevos resultados de la consulta en la cuadrícula.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Botón Actualizar perfil

Al hacer clic en el botón **Actualizar perfil** , se\_activa el procedimiento Sub de VBScript Update OnClick, que ejecuta el objeto RDS. DataControl () los métodos SubmitChanges y Refresh.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Cuando DC1. SubmitChanges se ejecuta, el servicio de datos remotos empaqueta toda la información de actualización y la envía al servidor mediante HTTP. La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado. , el servicio de datos remotos (RDS) empaqueta toda la información de actualización y la envía al servidor mediante HTTP. La actualización es todo o nada: si una parte de la actualización no es correcta, no se realiza ningún cambio y se devuelve un mensaje de estado. DC1. Refresh no es necesario después de **SubmitChanges** con el servicio de datos remoto, pero garantiza datos actualizados.

## <a name="cancel-changes-button"></a>Botón Cancelar cambios

Al hacer clic en **Cancelar cambios** , se\_activa el procedimiento Sub OnClick de VBScript, que ejecuta el objeto RDS. DataControl (método CancelUpdate).

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Cuando se ejecuta, descarta cualquier modificación que haya realizado un usuario en un registro de empleado en la cuadrícula de datos desde la última consulta o actualización. Restaura los valores originales.

