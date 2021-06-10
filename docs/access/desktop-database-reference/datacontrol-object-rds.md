---
title: Objeto DataControl (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294522"
---
# <a name="datacontrol-object-rds"></a>Objeto DataControl (RDS)

**Se aplica a:** Access 2013, Office 2013

Enlaza un objeto [Recordset](recordset-object-ado.md) de consulta de datos a uno o varios controles (por  ejemplo, un cuadro de texto, un control de cuadrícula o un cuadro combinado) para mostrar los datos recordset en una página web.

## <a name="syntax"></a>Sintaxis

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Comentarios

El identificador de clase para el objeto **RDS.DataSpace** es BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!NOTA] Si obtiene el error de que un objeto [RDS.DataSpace](dataspace-object-rds.md) o **RDS.DataControl** no se carga, asegúrese de estar utilizando el Id. de clase correcto. Los Id. de clase para estos objetos han cambiado desde las versiones 1.0 y 1.1.

En un escenario básico, solo hay que configurar las propiedades **SQL**, **Connect** y **Server** del objeto **RDS.DataControl**, que llamará automáticamente al objeto de negocio predeterminado, [RDSServer.DataFactory](datafactory-object-rdsserver.md).

Todas las propiedades del objeto **RDS.DataControl** son opcionales porque los objetos de negocio personalizados pueden reemplazar su funcionalidad.

> [!NOTE]
> [!NOTA] Si realiza una consulta para varios resultados, sólo se devuelve el primer objeto [Recordset](recordset-object-ado.md). Si necesita varios conjuntos de resultados, asigne cada uno a su propio objeto **DataControl**. 
> 
> Un ejemplo de una consulta para varios resultados podría ser el siguiente: `"Select * from Authors, Select * from Topics"` .

La adición de "DFMode=20;" a la cadena de conexión cuando se utiliza el objeto **RDS.DataControl** puede mejorar el rendimiento del servidor a la hora de actualizar datos. Con este valor, el objeto **RDSServer.DataFactory** del servidor utiliza un modo que emplea menos recursos. No obstante, en esta configuración no están disponibles las siguientes características:

  - Uso de consultas parametrizadas.

  - Obtención de información de parámetros o columnas antes de llamar al método **Execute**.

  - Establecimiento de **Transact Updates** en **True**.

  - Obtención del estado de fila.

  - Llamada al método [Resync](resync-method-ado.md).

  - Actualización (de forma explícita o automática) mediante la propiedad [Update Resync](update-resync-property-dynamic-ado.md).

  - Configuración de las propiedades **Command** o [Recordset](recordset-sourcerecordset-properties-rds.md).

  - Uso de **adCmdTableDirect**.

El objeto **RDS.DataControl** se ejecuta en modo asincrónico de forma predeterminada. Si necesita una ejecución sincrónica para la aplicación, establezca el parámetro [ExecuteOptions](executeoptions-property-rds.md) de modo que sea igual a **adcExecSync** y el parámetro [FetchOptions](fetchoptions-property-rds.md) de modo que sea igual a **adcFetchUpFront**, como se muestra en el ejemplo siguiente.

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

Use un objeto **RDS.DataControl** para vincular los resultados de una consulta única a uno o varios controles visuales. Por ejemplo, suponga que codifica una consulta que solicita datos de clientes como Nombre, Domicilio, Lugar de nacimiento, Edad y Estado de prioridad. Puede utilizar un objeto **RDS.DataControl** único para que se muestren el Nombre, la Edad y la Región de un cliente en tres cuadros de texto independientes; el Estado de prioridad en una casilla de verificación; y todos los datos en un control de cuadrícula.

Use objetos **RDS.DataControl** diferentes para vincular los resultados de varias consultas a controles visuales diferentes. Por ejemplo, suponga que utiliza una consulta para obtener información sobre un cliente y otra consulta para obtener información sobre los productos que el cliente ha comprado. Además, desea que los resultados de la primera consulta se muestren en tres cuadros de texto y una casilla de verificación, y que los resultados de la segunda consulta se muestren en un control de cuadrícula. Si utiliza el objeto de negocio predeterminado (**RDSServer.DataFactory**), tiene que realizar lo siguiente:

  - Agregue dos **RDS. DataControl objetos** a la página web.

  - Escribir dos consultas, una para cada propiedad **SQL** de los dos objetos **RDS.DataControl**. Un objeto **RDS.DataControl** contendrá una consulta SQL solicitando información del cliente, y el otro contendrá una consulta solicitando una lista de los productos que el cliente ha comprado.

  - En cada una de las etiquetas OBJECT de los controles dependientes, especifique el valor DATAFLD de modo que se establezcan los valores correspondientes a los datos que desea que se muestren en cada control visual.

No hay ninguna restricción de recuento en el número de **RDS. Objetos DataControl** que se pueden insertar a través de etiquetas OBJECT en una sola página web.

Al definir el **RDS. Objeto DataControl** en una página web, use valores **distintos** de cero Height y **Width,** como 1 (para evitar la inclusión de espacio adicional).

Los componentes del cliente de servicio de datos remotos ya están incluidos como parte de Internet Explorer 4.0; por lo tanto, no es necesario incluir un parámetro CODEBASE en la etiqueta del objeto **RDS.DataControl**.

Con Internet Explorer 4.0 o posterior, puede enlazar a datos mediante controles HTML y controles ActiveX solo si están marcados como controles de modelo de apartamento.

**Usuarios Visual Basic Microsoft** The **RDS. DataControl** solo se usa en aplicaciones basadas en web. Una aplicación de cliente de Visual Basic no lo necesita.

