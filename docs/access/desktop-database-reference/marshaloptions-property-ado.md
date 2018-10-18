---
<<<<<<< Título HEAD: MarshalOptions (propiedad) (ADO) TOCTitle: MarshalOptions (propiedad) (ADO) === título: MarshalOptions (propiedad, ADO) TOCTitle: MarshalOptions (propiedad, ADO)
>>>>>>> Master ms:assetid: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: ms.date 48548143: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="marshaloptions-property-ado"></a>MarshalOptions (propiedad, ADO)
=======
# <a name="marshaloptions-property-ado"></a>MarshalOptions (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica qué registros se van a ordenar de nuevo en el servidor.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.

## <a name="remarks"></a>Comentarios

<<<<<<< HEAD cuando se usa un [conjunto de registros](recordset-object-ado.md)de lado cliente, los registros que se han modificado en el cliente se vuelven a escribir el nivel intermedio o el servidor Web a través de una técnica denominada el cálculo de referencias, el proceso de empaquetado y envío de interfaz parámetros del método a través de límites de subproceso o proceso. Al establecer la propiedad **MarshalOptions**, se puede mejorar el rendimiento durante el cálculo de referencias de los datos remotos modificados para volver a actualizarse en el nivel intermedio o en el servidor web.
=== Cuando se usa un [conjunto de registros](recordset-object-ado.md)de lado cliente, los registros que se han modificado en el cliente se vuelven a escribir el nivel intermedio o el servidor web a través de una técnica denominada el cálculo de referencias, el proceso de empaquetar y enviar parámetros de métodos de interfaz a través de límites de subprocesos o procesos. Al establecer la propiedad **MarshalOptions** puede mejorar el rendimiento cuando datos remotos modificados se calculan las referencias para volver a actualizarse el nivel intermedio o el servidor web.
>>>>>>> master

**Uso de servicio de datos remotos** Esta propiedad se utiliza sólo en un **conjunto de registros**de lado cliente.

