---
<<<<<<< Título HEAD: CommandTimeout (propiedad) (ADO) TOCTitle: CommandTimeout (propiedad) (ADO) === título: CommandTimeout (propiedad, ADO) TOCTitle: CommandTimeout (propiedad, ADO)
>>>>>>> Master ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15) ms:contentKeyID: ms.date 48546714: 18/09/2015 mtps_version: Office.15 f1_keywords:
- ado210.chm1231124 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="commandtimeout-property-ado"></a>CommandTimeout (propiedad, ADO)
=======
# <a name="commandtimeout-property-ado"></a>CommandTimeout (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el tiempo que se va a esperar durante la ejecución de un comando para que finalice el intento y se genere un error.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long** que indica, en segundos, cuánto tiempo se va a esperar a que se ejecute un comando. El valor predeterminado es 30.

## <a name="remarks"></a>Comentarios

<<<<<<< HEAD Use la propiedad **CommandTimeout** en un objeto [Connection](connection-object-ado.md) o un objeto [Command](command-object-ado.md) para permitir la cancelación de una llamada al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) , debido a los retrasos de uso del servidor de tráfico o a la sobrecarga de red. Si el intervalo establecido en la propiedad **CommandTimeout** transcurre antes de que finalice la ejecución del comando, se genera un error y ADO cancela el comando. Si se establece el valor de la propiedad en cero, ADO esperará indefinidamente a que finalice la ejecución. Asegúrese de que el proveedor y el origen de datos en el que está escribiendo código admiten la funcionalidad **CommandTimeout**.
=== Usar la propiedad **CommandTimeout** en un objeto [Connection](connection-object-ado.md) o un objeto [Command](command-object-ado.md) para permitir la cancelación de una llamada al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) , debido a los retrasos de uso del servidor de tráfico o a la sobrecarga de red. Si el intervalo establecido en la propiedad **CommandTimeout** transcurre antes de que finalice la ejecución del comando, se genera un error y ADO cancela el comando. Si se establece el valor de la propiedad en cero, ADO esperará indefinidamente a que finalice la ejecución. Asegúrese de que el proveedor y el origen de datos en el que está escribiendo código admiten la funcionalidad **CommandTimeout**.
>>>>>>> master

La configuración de **CommandTimeout** en un objeto **Connection** no afecta a la configuración de **CommandTimeout** en un objeto **Command** del mismo objeto **Connection**; es decir, la propiedad **CommandTimeout** del objeto **Command** no hereda el valor de la propiedad **CommandTimeout** del objeto **Connection**.

En un objeto **Connection**, la propiedad **CommandTimeout** sigue siendo de lectura y escritura después de abrirse el objeto **Connection**.

