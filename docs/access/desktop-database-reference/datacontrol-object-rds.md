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
# <a name="datacontrol-object-rds"></a><span data-ttu-id="a5ae0-102">Objeto DataControl (RDS)</span><span class="sxs-lookup"><span data-stu-id="a5ae0-102">DataControl object (RDS)</span></span>

<span data-ttu-id="a5ae0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5ae0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5ae0-104">Enlaza un conjunto [](recordset-object-ado.md) de registros de consulta de datos a uno o varios controles (por ejemplo, un cuadro de texto, un control de cuadrícula o un cuadro combinado) para mostrar los datos del conjunto de registros en una página web. </span><span class="sxs-lookup"><span data-stu-id="a5ae0-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ae0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5ae0-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="a5ae0-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5ae0-106">Remarks</span></span>

<span data-ttu-id="a5ae0-107">El identificador de clase para el objeto **RDS.DataSpace** es BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="a5ae0-p101">[!NOTA] Si obtiene el error de que un objeto [RDS.DataSpace](dataspace-object-rds.md) o **RDS.DataControl** no se carga, asegúrese de estar utilizando el Id. de clase correcto. Los Id. de clase para estos objetos han cambiado desde las versiones 1.0 y 1.1.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p101">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID. The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="a5ae0-110">En un escenario básico, solo hay que configurar las propiedades **SQL**, **Connect** y **Server** del objeto **RDS.DataControl**, que llamará automáticamente al objeto de negocio predeterminado, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="a5ae0-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="a5ae0-111">Todas las propiedades del objeto **RDS.DataControl** son opcionales porque los objetos de negocio personalizados pueden reemplazar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="a5ae0-112">[!NOTA] Si realiza una consulta para varios resultados, sólo se devuelve el primer objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5ae0-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="a5ae0-113">Si necesita varios conjuntos de resultados, asigne cada uno a su propio objeto **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="a5ae0-114">Un ejemplo de una consulta para varios resultados podría ser el siguiente: `"Select * from Authors, Select * from Topics"` .</span><span class="sxs-lookup"><span data-stu-id="a5ae0-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="a5ae0-p103">La adición de "DFMode=20;" a la cadena de conexión cuando se utiliza el objeto **RDS.DataControl** puede mejorar el rendimiento del servidor a la hora de actualizar datos. Con este valor, el objeto **RDSServer.DataFactory** del servidor utiliza un modo que emplea menos recursos. No obstante, en esta configuración no están disponibles las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p103">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data. With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode. However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="a5ae0-118">Uso de consultas parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="a5ae0-119">Obtención de información de parámetros o columnas antes de llamar al método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="a5ae0-120">Establecimiento de **Transact Updates** en **True**.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="a5ae0-121">Obtención del estado de fila.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-121">Getting row status.</span></span>

  - <span data-ttu-id="a5ae0-122">Llamada al método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5ae0-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="a5ae0-123">Actualización (de forma explícita o automática) mediante la propiedad [Update Resync](update-resync-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5ae0-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="a5ae0-124">Configuración de las propiedades **Command** o [Recordset](recordset-sourcerecordset-properties-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a5ae0-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="a5ae0-125">Uso de **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="a5ae0-p104">El objeto **RDS.DataControl** se ejecuta en modo asincrónico de forma predeterminada. Si necesita una ejecución sincrónica para la aplicación, establezca el parámetro [ExecuteOptions](executeoptions-property-rds.md) de modo que sea igual a **adcExecSync** y el parámetro [FetchOptions](fetchoptions-property-rds.md) de modo que sea igual a **adcFetchUpFront**, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p104">The **RDS.DataControl** object runs in asynchronous mode by default. If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

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

<span data-ttu-id="a5ae0-p105">Use un objeto **RDS.DataControl** para vincular los resultados de una consulta única a uno o varios controles visuales. Por ejemplo, suponga que codifica una consulta que solicita datos de clientes como Nombre, Domicilio, Lugar de nacimiento, Edad y Estado de prioridad. Puede utilizar un objeto **RDS.DataControl** único para que se muestren el Nombre, la Edad y la Región de un cliente en tres cuadros de texto independientes; el Estado de prioridad en una casilla de verificación; y todos los datos en un control de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p105">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls. For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status. You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="a5ae0-p106">Use objetos **RDS.DataControl** diferentes para vincular los resultados de varias consultas a controles visuales diferentes. Por ejemplo, suponga que utiliza una consulta para obtener información sobre un cliente y otra consulta para obtener información sobre los productos que el cliente ha comprado. Además, desea que los resultados de la primera consulta se muestren en tres cuadros de texto y una casilla de verificación, y que los resultados de la segunda consulta se muestren en un control de cuadrícula. Si utiliza el objeto de negocio predeterminado (**RDSServer.DataFactory**), tiene que realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p106">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls. For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased. You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control. If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="a5ae0-135">Agregue dos **RDS. Objetos DataControl** de la página web.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="a5ae0-p107">Escribir dos consultas, una para cada propiedad **SQL** de los dos objetos **RDS.DataControl**. Un objeto **RDS.DataControl** contendrá una consulta SQL solicitando información del cliente, y el otro contendrá una consulta solicitando una lista de los productos que el cliente ha comprado.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-p107">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="a5ae0-138">En cada una de las etiquetas OBJECT de los controles dependientes, especifique el valor DATAFLD de modo que se establezcan los valores correspondientes a los datos que desea que se muestren en cada control visual.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="a5ae0-139">No hay ninguna restricción de recuento en el número de **RDS. Objetos DataControl** que se pueden insertar a través de etiquetas OBJECT en una sola página web.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="a5ae0-140">Al definir **rds. Objeto DataControl** en una página web, use valores **de alto** y ancho distintos de cero, como 1 (para evitar la inclusión de espacio adicional). </span><span class="sxs-lookup"><span data-stu-id="a5ae0-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="a5ae0-141">Los componentes del cliente de servicio de datos remotos ya están incluidos como parte de Internet Explorer 4.0; por lo tanto, no es necesario incluir un parámetro CODEBASE en la etiqueta del objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="a5ae0-142">Con Internet Explorer 4.0 o posterior, puedes enlazar a datos mediante controles HTML y controles ActiveX solo si están marcados como controles de modelo de departamentos.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="a5ae0-143">**Usuarios de Microsoft Visual Basic** The **RDS. DataControl** solo se usa en aplicaciones basadas en web.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="a5ae0-144">Una aplicación de cliente de Visual Basic no lo necesita.</span><span class="sxs-lookup"><span data-stu-id="a5ae0-144">A Visual Basic client application has no need for it.</span></span>

