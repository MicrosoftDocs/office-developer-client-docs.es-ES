---
title: BuscarRegistro (acción de macro)
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 19b6c80af2bcee9ca3dbe51bbbcf56343f33d550
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937613"
---
# <a name="findrecord-macro-action"></a>BuscarRegistro (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **BuscarRegistro** para buscar la primera instancia de los datos que cumplan los criterios especificados por los argumentos de **BuscarRegistro**. Estos datos se pueden encontrar en el registro activo, en un registro anterior o posterior, o bien, en el primer registro. Puede buscar registros en la hoja de datos de la tabla, la hoja de datos de la consulta, la hoja de datos del formulario o el formulario que esté activo.

## <a name="setting"></a>Configuración

La acción **BuscarRegistro** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Buscar</strong></p></td>
<td><p>Especifica los datos que se desean buscar en el registro. Escriba el texto, número o fecha que desea buscar o escriba una expresión, está precedida por un signo igual (<strong>=</strong>), en el cuadro <strong>Buscar</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Puede usar caracteres comodín. Este argumento es necesario.</p></td>
</tr>
<tr class="even">
<td><p><strong>Coincidir</strong></p></td>
<td><p>Especifica dónde están ubicados los datos en el campo. Puede especificar una búsqueda de datos en cualquier parte del campo (<strong>Cualquier parte del campo</strong>), datos que llenen todo el campo (<strong>Hacer coincidir todo el campo</strong>) o datos ubicados al principio del campo (<strong>Comienzo del campo</strong>). El valor predeterminado es <strong>Hacer coincidir todo el campo</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Coincidir mayúsculas y minúsculas</strong></p></td>
<td><p>Especifica si en la búsqueda se hace distinción de mayúsculas y minúsculas. Haga clic en <strong>Sí</strong> (para llevar a cabo una búsqueda en la que coincidan las mayúsculas y minúsculas) o <strong>No</strong> (para buscar sin que coincidan exactamente las letras mayúsculas y minúsculas). El valor predeterminado es <strong>No</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Buscar</strong></p></td>
<td><p>Especifica si la búsqueda se produce desde el registro activo hacia el principio de los registros (<strong>Arriba</strong>), hacia abajo hasta el final de los registros (<strong>Abajo</strong>), o bien, desde el registro activo hacia el final de los registros y luego desde el principio de los registros hasta el registro activo, de forma que se busque en todos los registros (<strong>Todos</strong>). El valor predeterminado es <strong>Todos</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Buscar con formato</strong></p></td>
<td><p>Especifica si la búsqueda incluye datos con formato. Haga clic en <strong>Sí</strong> (Microsoft Office Access 2007 busca los datos con el formato y tal y como se muestran en el campo) o <strong>No</strong> (Access busca los datos tal y cómo se almacenan en la base de datos, que no siempre son los mismos que se muestran). El valor predeterminado es <strong>No</strong>. Puede usar esta característica para restringir la búsqueda a los datos con un formato concreto. Por ejemplo, haga clic en <strong>Sí</strong> y escriba <strong>1,234</strong> en el argumento <strong>Buscar</strong> para buscar un valor de 1,234 en el campo con formato para incluir comas. Haga clic en <strong>No</strong> si quiere escribir <strong>1234</strong> para buscar los datos de este campo. Para buscar fechas, haga clic en <strong>Sí</strong> para buscar una fecha exacta con el formato exacto, como 08-Julio-2003. Si hace clic en <strong>No</strong>, escriba la fecha para el argumento <strong>Buscar</strong> con el formato configurado en la configuración regional del Panel de control de Windows. Este formato se muestra en el cuadro <strong>Formato de fecha corta</strong> de la pestaña <strong>Fecha</strong> de la configuración regional. Por ejemplo, si el cuadro <strong>Formato de fecha corta</strong> está configurado en <strong>M/d/aa</strong>, puede escribir 7/8/03 y Access buscará todas las entradas de un campo Fecha que se correspondan al 8 de julio de 2003, independientemente del formato que tenga el campo.  </p>

> [!NOTE]
> El argumento **Buscar con formato** sólo tiene efecto si el campo activo es un control dependiente, el argumento **Coincidir** está establecido en **Hacer coincidir todo el campo**, el argumento **Sólo el campo activo** está establecido en **Sí** y el argumento **Coincidir mayúsculas y minúsculas** está establecido en **No**.


<p>

					Si establece <strong>Coincidir mayúsculas y minúsculas</strong> en <strong>Sí</strong> o <strong>Sólo el campo activo</strong> en <strong>No</strong>, también debe establecer <strong>Buscar con formato</strong> en <strong>Sí</strong>.

</p></td>
</tr>
<tr class="even">
<td><p><strong>Sólo campo activo</strong></p></td>
<td><p>Especifica si la búsqueda está restringida al campo activo en cada registro o si incluye todos los campos. La búsqueda en el campo activo es más rápida. Haga clic en <strong>Sí</strong> (restringir búsqueda a campo activo) o <strong>No</strong> (búsqueda en todos los campos en cada registro). El valor predeterminado es <strong>Sí</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Buscar primero</strong></p></td>
<td><p>Especifica si la búsqueda comienza en el primer registro o en el registro activo. Haga clic en <strong>Sí</strong> (para empezar en el primer registro) o <strong>No</strong> (para empezar en el registro activo). El valor predeterminado es <strong>Sí</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Cuando una macro ejecuta la acción **BuscarRegistro**, Access busca los datos especificados en los registros (el orden de la búsqueda viene determinado por el valor del argumento **Buscar** ). Cuando Access encuentra los datos especificados, se seleccionan los datos en el registro.

La acción **BuscarRegistro** es equivalente a hacer clic en **Buscar** en la ficha **Inicio**, y sus argumentos son los mismos que las opciones del cuadro de diálogo **Buscar y reemplazar**. Si establece los argumentos de **BuscarRegistro** en el panel Generador de macros y, a continuación, ejecuta la macro, verá las correspondientes opciones seleccionadas en el cuadro de diálogo **Buscar y reemplazar** cuando haga clic en **Buscar**.

Access conserva los argumentos más recientes de **BuscarRegistro** durante una sesión de la base de datos, por lo que no es necesario escribir repetidas veces los mismos criterios cuando se realizan operaciones posteriores con la acción **BuscarRegistro**. Si deja un argumento en blanco, Access utiliza el valor más reciente del argumento, establecido por una acción **BuscarRegistro** anterior o en el cuadro de diálogo **Buscar y reemplazar**.

Cuando desee buscar un registro mediante una macro, utilice la acción **BuscarRegistro** en lugar de la acción **EjecutarComandoDeMenú** con su argumento establecido para que se ejecute el comando **Buscar**.

> [!NOTE]
> [!NOTA] Si bien la acción **BuscarRegistro** corresponde al comando **Buscar** en la ficha **Inicio** de tablas, consultas y formularios, no corresponde al comando **Buscar** del menú **Edición** en la ventana Código. No se puede utilizar la acción **BuscarRegistro** para buscar texto en módulos.

Si el texto actualmente seleccionado es el mismo que el texto seleccionado en el momento en el que se ejecuta la acción **BuscarRegistro**, la búsqueda se inicia inmediatamente después de la selección en el mismo campo que la selección y en el mismo registro. En caso contrario, la búsqueda se inicia al principio del registro actual. Esto permite buscar múltiples instancias de los mismos criterios de búsqueda que pudieran aparecer en un único registro.

Sin embargo, observe que si usa un botón de comando para ejecutar una macro que contenga la acción **BuscarRegistro**, se buscará de forma repetida la primera instancia de los criterios de búsqueda. Este comportamiento se debe a que, al hacer clic en el botón de comando, se quita el enfoque del campo que contiene el valor coincidente. La acción **BuscarRegistro** empezará la búsqueda desde el principio del registro. Para evitar este problema, ejecute la macro usando una técnica que no cambie el enfoque, como un botón de una barra de herramientas personalizada o una combinación de teclas definida en una macro AutoKeys. O bien, establezca el enfoque de la macro en el campo que contiene los criterios de búsqueda antes de llevar a cabo la acción **BuscarRegistro**.

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Nota de seguridad" alt="Security note" />de seguridad**</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      No use la declaración <strong>SendKeys</strong> ni una macro AutoKeys con información sensible o confidencial porque un usuario malintencionado podría interceptar las pulsaciones de teclas y vulnerar la seguridad de su equipo y de sus datos.
</td>
</tr>
</tbody>
</table>

El mismo comportamiento se produce si usa un botón de comando para ejecutar una macro que contenga la acción **BuscarSiguiente**.

Para ejecutar la acción **BuscarRegistro** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **FindRecord** del objeto **DoCmd**.

Para realizar búsquedas más complejas, conviene usar la macro de acción **EncontrarRegistro**.

